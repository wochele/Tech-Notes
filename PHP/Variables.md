# Variables

### Background

- Variables are case-sensitive
- Names begin with a $
- Ints which exceed the max num are converted to a float
- Type does not need to be declared

#### Octal

- Begin with a 0

#### Hex

- Begin with 0x

#### Binary

- Begin with 0b

#### Float

- `$float = 1.23434` or scientific notation `$float = 1.234E4`

#### Boolean

- `$bool = true;` or `$bool = false;`
- Convert to a boolean `var_dump((bool)$intVar);`

#### Finding the type of variable

- `is_int()` `is_string()` `is_bool()` `is_float()`

#### Static Variables

Static variables declared inside a function keep their value between function calls

    static $count = 0;

### Superglobal Variables

| Name | Contents |
|------|----------|
| $GLOBALS | All variables in current scope. Variable names are keys of the array |
| $_SERVER | Headers, paths and script locations. Created by web server. |
| [$_GET](http://php.net/manual/en/reserved.variables.get.php) | Variables passed via HTTP Get method |
| [$_POST](http://php.net/manual/en/reserved.variables.post.php) | Variables passed via HTTP Post method |
| $_FILES | Items uploaded via HTTP Post method |
| $_COOKIE | Variables passed via HTTP cookie |
| $_SESSION | Session variables available |
| $_REQUEST | Contents on information passed from browser |
| $_ENV | Variables passed via environment method |

```php
echo 'Hello ' . htmlspecialchars($_GET["name"]) . '!';
```

### View variable values for troubleshooting

```php
<pre><?php print_r($_GET);?></pre> // Place at top of page
```

### Get Method

    /test/demo_form.asp?name1=value1&name2=value2

- Length restrictions
- Can be bookmarked

### Post Method

- No length restrictions
- Cannot be bookmarked

