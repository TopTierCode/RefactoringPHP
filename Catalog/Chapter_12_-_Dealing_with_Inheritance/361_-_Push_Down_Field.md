# Push Down Field (361)

Inverse of [Pull Up Field (353)](353_-_Pull_Up_Field.md)

## Old Code

```php
<?php
class Employee
{
    protected string $quota;
}

class Engineer extends Employee
{
    ...
}

class Salesman extends Employee
{
    ...
}
```

## New Code

```php
<?php
class Employee
{
    ...
}

class Engineer extends Employee
{
    ...
}

class Salesman extends Employee
{
    private string $quota;
}
```