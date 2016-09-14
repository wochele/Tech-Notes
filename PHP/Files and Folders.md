# Files and Folders

### Including files

```php
include 'FILENAME.php';
include_once 'FILENAME.php';  //For class file because they can't be included more than once

//Require will terminate the script execution if the file cannot be found
require 'FILENAME.php';
require_once 'FILENAME.php';  //For class file because they can't be included more than once

```

- Name files the same as the class they contain

#### [Get Current Working Directory](http://php.net/manual/en/function.getcwd.php)

```php
// current directory
echo getcwd() . "\n";
```

#### Using GLOB to Parse Filenames

[Loop Through Folders with PHP's Glob](http://code.tutsplus.com/tutorials/quick-tip-loop-through-folders-with-phps-glob--net-11274)
