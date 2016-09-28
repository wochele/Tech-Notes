# Control Structures

#### For-Each loop

```php
foreach($array as $item) {
    echo $item."\n";
}
```

foreach for an associative array

```php
foreach($array as $key => $item) {
    echo $item." (".$key.")\n";
}
```

### If Statement

```php
if(CONDITION) {
    //Code to execute
}
else {
    //Code to execute 
}
```

### If Else Statement

```php
if(CONDITION) {
    //Code to execute
}
elseif (CONDITION) {
    //Code to execute
}
else {
    //Code to execute 
}
```

### Switch Statement

```php
switch ($var){
    case 0:
        //Code to execute
        break;
    case 1:
        //Code to execute 
        break;
    default:
        //Code to execute
        break;  
}
```

### Ternary Operator

- (expr1) ? (expr2) : (expr3);
- `$var = (T/F expression) ? (Return Exp if True) : (Return Exp if False);`

### Null Coalesce Operator

- `$var = $count ?? (Expression);`
- If true, return count. If false, return expression. 
- Good for checking if a variable has been set. Maybe in a web form. 
- Can be chained together.

### While Loop

```php
while(expr) {
    //code to execute
}
```

### For Loop

```php
for($i = 0; $i < 5; $i++) {

}
```

