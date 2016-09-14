# Constants

### Defining a Constant

```php
define("ROOT_LOCATION", "/usr/local/www/");
```

- Constants do not use $
- Convention has the names as all-uppercase and spaces as _
- Must be created with the define() function
- Are global and can be accessed anywhere
- Check if a constant is defined `defined('CONST_NAME')` - Single quotes must be used

### Predefined constants

| Constant | Description |
|----------|-------------|
| `__LINE__` | Current line # of the file |
| `__FILE__` | Full path and filename of the file |
| `__DIR__` | Directory of the file |
| `__FUNCTION__` | Function Name |
| `__CLASS__` | Class name Name |
| `__METHOD__` | Class method name Name |
| `__NAMESPACE__` | Name of current namespace |
