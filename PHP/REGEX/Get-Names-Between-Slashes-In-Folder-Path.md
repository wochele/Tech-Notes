# PHP - Get all strings between slashes in a string (path)

[regex in php to get two strings between slashes](http://stackoverflow.com/questions/18725084/regex-in-php-to-get-two-strings-between-slashes)

```php
$test = "/foo/XXX/bar/YYY/";

// Remove slash from beginning and end of the string
$test = trim($test, '/');

$arr = explode('/', $test);
print_r($arr);
```

returns
```php
Array
(
  [0] => foo 
  [1] => XXX 
  [2] => bar 
  [3] => YYY 
)
```
