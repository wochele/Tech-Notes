# Including Files in PHP

### Including files

```php
include 'FILENAME.php';
include_once 'FILENAME.php';  //For class file because they can't be included more than once

//Require will terminate the script execution if the file cannot be found
require 'FILENAME.php';
require_once 'FILENAME.php';  //For class file because they can't be included more than once

```

- Name files the same as the class they contain
