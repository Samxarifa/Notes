## Connect to SQL

### Using PDO (PHP Database Object) With MySQL

```php
function connectToDB() {
	$server = 'mysql:host={ip};dbname={db}';
	$username = '{username}';
	$password = '{password}';
	
	$db = new PDO($server,$username,$password);
	return $db;
    }
```

### Connect and Run Command

```php
$db = connectToDB();

$sql = "{sql}";
$query = $db->prepare($sql);

$query->bindParam(':sqlParam1',$value1);
$query->bindParam(':sqlParam2',$value2);

$query->execute();
$db = null;
```

### Get all Results

```php
while ($row = $query->fetch()) {
	...
}
```

### Get 1 Result

```php
if ($query->rowCount() == 1) {
	$row = $query->fetch();
	...
} else {
	...
}
```
