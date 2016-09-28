# Working with folders in PHP

### [Get Current Working Directory](http://php.net/manual/en/function.getcwd.php)

```php
// current directory
echo getcwd() . "\n";
```

### Using `glob()` to Parse Filenames

[Loop Through Folders with PHP's Glob](http://code.tutsplus.com/tutorials/quick-tip-loop-through-folders-with-phps-glob--net-11274)

```php
foreach(glob('userImages/*/TN/*') as $image) {	
	echo "Filename: " . $image . "<br />";	
}

OUTPUT:
Filename: userImages/username1/TN/test.jpg
Filename: userImages/username1/TN/test3.jpg
Filename: userImages/username1/TN/test5.png
Filename: userImages/username2/TN/subfolder
Filename: userImages/username2/TN/test2.jpg
Filename: userImages/username2/TN/test4.gif
Filename: userImages/username3/TN/styles.css
```

```php
foreach(glob('userImages/*/TN/*.jpg') as $image) {	
	echo "Filename: " . $image . "<br />";	
}

OUTPUT:
Filename: userImages/username1/TN/test.jpg
Filename: userImages/username1/TN/test3.jpg
Filename: userImages/username2/TN/test2.jpg
```

### Using an argument with `glob()`

- *GLOB_MARK*: Adds a slash to each directory returned
- *GLOB_NOSORT*: Return files as they appear in the directory (no sorting)
- *GLOB_NOCHECK*: Return the search pattern if no files matching it were found
- *GLOB_NOESCAPE*: Backslashes do not quote metacharacters
- *GLOB_BRACE*: Expands {a,b,c} to match 'a', 'b', or 'c'
- *GLOB_ONLYDIR*: Return only directory entries which match the pattern
- *GLOB_ERR*: Stop on read errors (like unreadable directories), by default errors are ignored

```php
foreach(glob('userImages/*/TN/{*.jpg,*.gif}', GLOB_BRACE) as $image) {
	echo "Filename: " . $image . "<br />";	
}

OUTPUT:
Filename: userImages/username1/TN/test.jpg
Filename: userImages/username1/TN/test3.jpg
Filename: userImages/username2/TN/test2.jpg
Filename: userImages/username2/TN/test4.gif
```
