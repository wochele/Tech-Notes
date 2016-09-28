# String Manipulation

#### String to Upper

```php
strtoupper($var);
```

#### String to Lower

```php
strtolower($var);
```

#### Get length of string

```php
strlen($var); // Returns length of the string $var
```

#### Get last character of a string

```php
substr($string, -1) 

// Or with direct string access
$string[strlen($string)-1];
```

#### String position

```php
strpos($var, $strtosearch[,OFFSET_OF_WHERE_TO_SEARCH])
```

- Case sensitive
- Empty string is returned if the pattern is not found

#### String replace

```php
str_replace($valToReplace, $ReplacementValue, $stringToSearch[,$numReplaced]);
```

- `$numReplaced` is a pass by reference variable and is declared in the function call

#### Substring

```php
substr($substringSource, $startLocOfSubstring[, $numCharsToRetrieve])
```

- A negative number for $startLocOfSubstring will start that many from the end of the string.
- A negative number for $numCharsToRetrieve will end the substring that many from the end

#### String Split

```php
$varArray = str_split($quote[,$chunkLength])
```

- Converts a string to an array
- Can be printed with `print_r($varArray)`
- Optional parameter breaks up string into x length chunks

#### Remove First X Characters From a String

```php
$str = "The quick brown fox jumps over the lazy dog."
$str2 = substr($str, 4); // "quick brown fox jumps over the lazy dog."
```

- [Remove first 4 characters of a string php](http://stackoverflow.com/questions/4286423/remove-first-4-characters-of-a-string-php)

