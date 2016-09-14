# mySQL

### Resources

- ['MySQLi' for Beginners](http://codular.com/php-mysqli)
- [How to Use PHP Improved MySQLi extension](http://www.pontikis.net/blog/how-to-use-php-improved-mysqli-extension-and-why-you-should)

### Connect to the Database

```php
//Connection variables
$dbPassword = "PASSWORD";
$dbUserName = "USERNAME";
$dbServer = "SERVER ADDRESS";
$dbName = "DB NAME";

$connection = new mysqli($dbServer, $dbUserName, $dbPassword, $dbName);

if($connection->connect_errno) {
    exit("Database Connection Failed. Reason: ".$connection->connect_error);
}

// Close the db connection 

$connection->close();
```

### Delete Entry from Database

```php
$query = "DELETE FROM DB_NAME WHERE id = 4";

$connection->query($query);
```

### Update Entry in Database

```php
$query = "UPDATE DB_NAME SET FIELD_NAME = 'string' WHERE id = 2";

$connection->query($query);
```

### Insert Entry in Database

```php
$query = "INSERT INTO DB_NAME (FIELD1, FIELD2, FIELD3) VALUES ('value1', 'value2', 'value3')";

$connection->query($query);
```

### Get ID of Newly Inserted Row

```php
$query = "INSERT INTO DB_NAME (FIELD1, FIELD2, FIELD3) VALUES {'value1', 'value2', 'value3'}";

$connection->query($query);

echo "New ID: ".$connection->insert_id;
```

### Select Data from Database

```php
$query = "SELECT FIELD1, FIELD2, FIELD3 FROM DB_NAME ORDER BY FIELD1";

$resultObj = $connection->query($query);

if($resultObj->num_rows > 0) {
    while($singleRowFromQuery = $resultObj->fetch_assoc()) {
        echo "Info: ".$singleRowFromQuery['FIELD1'].PHP_EOL;
    }
}

// Close result object after using
$resultObj->close();
```

### Using Prepared Statements

```php
// ? is a placeholder to send value later
$query = "SELECT FIELD1, FIELD2, FIELD3 FROM DB_NAME WHERE FIELD1 = ?";
$statementObj = $connection->prepare($query);

$statementObj->bind_param("sdi", $tempString, $tempFloat, $tempInt);
$statementObj->execute();

$statementObj->bind_results($info1, $info2, $info3);
$statementObj->store_result();

```

[php.net - prepared statements](http://php.net/manual/en/mysqli.quickstart.prepared-statements.php)

i
corresponding variable has type integer

d
corresponding variable has type double

s
corresponding variable has type string

b
corresponding variable is a blob and will be sent in packets
