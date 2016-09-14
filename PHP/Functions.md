# Functions

### Background

- Function names are not case-sensitive
- Can be called before the function is declared

#### Function syntax

```php
function createName($parameter1, $parameter2) {
    // function stuff here
}
```

### Default Parameters

```php
function createName($parameter1, $parameter2 = 2000) {
    // function stuff here
}
```

- Default parameters need to be the last parameters and required need to be at the beginning

#### Returning Values

```php
function createName($parameter1, $parameter2) {
    // function stuff here
    return $value;
}

$name = createName($first, $last);
```

#### Call function with variable

```php
function createName() {
    // function stuff here
}

$variableFunctionName = "createName";

$variableFunctionName();
```

#### Global Variable

```php
function createName($parameter1, $parameter2) {
    global $varName;
}
```

- `global` makes the variable global outside the function, globals declared outside the function are not visible inside the function 

#### Static keyword in a class function definition

To enable our method to be called without needing an object, we add the static keyword to the method definition. This allows the method to be called directly without specifying an object:

`public static function getById( $id ) {`



