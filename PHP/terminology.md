# Terminology

## Concrete Class

The class which implements an interface is called the Concrete Class.

Example

```php
interface BarInterface
{
    public function doTheThing(): string;
}

class Bar implements BarInterface
{
    public function doTheThing(): string
    {
        return 'Did the thing';
    }
}
```

## Abstraction

Data Abstraction is the most important features of any OOP programming language.

Flexibility comes from good abstractions, and not from inheritance.

## Inheritance

In OOP, inheritance is when a class derives from another class.

The child class will inherit all the public and protected properties and methods from the parent class. In addition, it can have its own properties and methods.

An inherited class is defined by using the `extends` keyword.

## Encapsulation

It shows only useful information, remaining are hidden from the end user.

## Implementation

TBD

---

Sources:

- [Encapsulation and Abstraction](https://www.thinktocode.com/2017/11/06/clean-code-php-abstraction-encapsulation/)
- [When to declare classes final](https://ocramius.github.io/blog/when-to-declare-classes-final/)
