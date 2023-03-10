## References

W3Schools: [SQL Tutorial](https://www.w3schools.com/sql/default.asp)

## Create Table

```sql
CREATE TABLE table_name (
field1 VARCHAR(20) NOT NULL AUTO-INCREMENT,
field2 INT,
field3 BOOL,
field4 INT,

PRIMARY KEY (field1),
FOREIGN KEY (field2) REFERENCES other_table(field2)
);
```


## Insert Into Table

```sql
INSERT INTO table_name (field1, field2, field3)
VALUES (value1, value2, value3);
```


## Show Data 

```sql
SELECT * FROM table_name;
```

```sql
SELECT field1, field2
FROM table_name
WHERE condition
ORDER BY ... 
GROUP BY ...
HAVING ... ;
```


## Update Data

```sql
UPDATE table_name
SET field1 = value1, field2 = value2...
WHERE condition;
```


## Delete Data

```sql
DELETE FROM table_name
WHERE condition;
```
