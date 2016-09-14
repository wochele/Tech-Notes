# Classes

### Background

- Class names are not case-sensitive
 
### Class Structure

```php
class Person {
    const AVG_LIFE_SPAN = 79;

    public $firstName = "Samuel Langhorn"; 
    public $lastName = "Clemens";
    public $yearBorn;
    
    function __construct() {
        $this->yearBorn = 1899;
    }
    
    // Or constructor can have variables
    function __construct($tempFirst = "", $tempLast = "", $tempBorn = ""){
        $this->firstName = $tempFirst;
        $this->lastName = $tempLast;
        $this->yearBorn = $tempBorn;
    }
    
    public function getFirstName() {
        return $this->firstName;
    }
    
    public function setFirstName($tempName) {
        $this->firstName = $tempName;
    }
}

//Create an object based on Person
$myObject = new Person();

$myObject->setFirstName("Sam");
```

- Container to put stuff in and retrieve stuff from

#### Properties

- Must be declared as public, private or protected
- Normally declared at the top of the class 
- Properties are accessed with `->` and do not include the $ 
    - `$myObject->firstName;`
- Set a property
    - `$myObject->firstName = "S. L.";`

#### Using constants in a class 

- Use the `const` keyword
- Can be an equation, but can't use any of the declared properties
- Names are all-caps with underscores between words
- Accessing the constant 
    - `$myObject::AVG_LIFE_SPAN;`
    - `Person::AVG_LIFE_SPAN;`
    
#### Using methods in a class 

- Methods are functions in a class 
- Methods default to public even
- Methods are accessed with `->`

#### Constructor

- `__construct` is the reserved word for a constructor declaration

#### Protected properties and methods

- Can only be accessed inside the class and descendents

#### Private properties and methods

- Can only be accessed in the class they are declared in 

#### Static properties and methods 

- Static is associated with the class and not instances of the class 

### Creating objects from classes

```php
$myObject = new Person();
```
