# Strings

#### Single quoted strings

- Variables are not expanded
- To use a single quote in the string put a backslash (\) in front of it
- Will print out escape sequences instead of evaluating them

#### Double quoted strings

- Variables are evaluated in printed in the string 
- To evaluate a variable in the middle of a string, use {}
    - `$var = "{$variable}nd place";`
- Single quotes will print just fine
- To use a double quote in the string put a backslash (\) in front of it
- Escape sequences are evaluated 

- Strings can be catenated together with `.`
    - `echo $var."nd place";`
    
#### Here Document (Here Doc)

```php
echo <<<EOT
   asl;dkjfa;ifea;
   lasdjfiweifj 
      asldkfja;woiej
      a;lsdkjfa;lsdkjfa 
      asfaskld
    alskdjfao;sidj
    aslkdfjaisodjfalsidjfias
EOT;
```

- Used to print a large area of text formatted in a specific way
- `<<<` followed by an identifier that will not appear in the text 
- At the end, the identifier must be on it's own line followed by ;

#### print vs echo 

- Use either (echo might be slightly faster)
- echo can take multiple strings separated by commas
- Paranthesis not needed since they are language constructs and not functions
