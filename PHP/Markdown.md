# Markdown in PHP

### Parsedown - Markdown parser for PHP

- [Parsedown Github](https://github.com/erusev/parsedown)
- [Parsedown Extra Github](https://github.com/erusev/parsedown-extra)

Include the parsedown files:
```
include("Parsedown.php");
include("ParsedownExtra.php");
```

Example:
```php
$Parsedown = new Parsedown();

echo $Parsedown->text('Hello _Parsedown_!'); # prints: <p>Hello <em>Parsedown</em>!</p>
```
