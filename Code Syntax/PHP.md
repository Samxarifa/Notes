## Check for Errors

Use ini_set to show errors and warnings for php code

```php
ini_set("display_errors",1);
ini_set("display_warnings",1);
```

## Connect to SQL

### Using PDO (PHP Database Object) With MySQL

This would usually be put in a separete php file called connect.php

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
