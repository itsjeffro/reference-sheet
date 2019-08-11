# Variable function

## Example

```
class Foo
{
    public function bar()
    {
        return 'foobar';
    }
}

$foo = new Foo;
$method = 'bar';

echo $foo->{$method}();
```

## Use cases

Curly braces may also be used, to clearly delimit the 
property name. They are most useful when accessing values 
within a property that contains an array, when the property 
name is made of multiple parts, or when the property name 
contains characters that are not otherwise valid.

## Further reading

- https://www.php.net/manual/en/language.variables.variable.php
- https://www.php.net/manual/en/migration70.incompatible.php#migration70.incompatible.variable-handling.indirect