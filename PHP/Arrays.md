# Arrays

### Add item to array

```php
$stack = array["orange", "banana"];
array_push[$stack, "apple", "raspberry"];
```

### Check if value exists in array

`in_array($valueToFind, $array[,$typeSame])` - $typeSame is a bool

### Add value to array

`$array[] = $valToAdd;`

- Array is created if it does not exist
- Will only add indexed values

`array['key'] = $valueToAdd;`

- Add value to associative array 


### Remove the last value from an array

`array_pop($array);`


### Remove specific item from array

`unset($array['value'][,...]);` - Array items can be chained together

- If unset is used with the entire array, it will be completely removed as if it never existed. Could be used on other types to remove them as well.

### Sorting Arrays

- Sort an indexed array
    - `sort($array);`
    - Additional info on sort [here](http://php.net/manual/en/function.sort.php)
- Sort an associative array 
    - `sort($array);'
        - This will sort the array but the result will be an indexed array 
    - `asort($array);'
        - Additional information on asort [here](http://php.net/manual/en/function.asort.php)
        - Maintains the index association
    - `ksort($array);'
        - Sorts the keys
        - Additional information on ksort [here](http://php.net/manual/en/function.ksort.php)
        
### Counting Items in an Array

`count($array);'

- Counts the number of items in an array
- For more options including counting multi-dimensional arrays, click [here](http://php.net/manual/en/function.count.php)

### Multi-Dimensional Arrays

[php.net - Arrays](http://php.net/manual/en/language.types.array.php)

### [Echo array](http://stackoverflow.com/questions/9816889/how-to-echo-an-array-in-php)

```php
echo '<pre>'; print_r($array); echo '</pre>'
```
#### Printing an Array

`print_r($array);`

### Initialize array

```php
$var = array();
```

### Associative Arrays

```php
$authors = array[
    "quarky" => "Charles Dickens",
    "brilliant" => "Jane Austin",
    "poetic" => "William Shakespear"
];
```

- Not indexed by numbers
- Keys can be strings or integers
- Value without specified key will get the next integer 

#### Accessing the array

`$authors['quarky'];`

#### Check if a key exists

`array_key_exists($key, $array);`
