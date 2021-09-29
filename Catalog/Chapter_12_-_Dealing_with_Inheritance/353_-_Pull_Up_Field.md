# Pull Up Field (353)

Inverse of [Push Down Field (361)](361_-_Push_Down_Field.md)

## Old Code

```php
<?php
class Employee
{
    ...
}

class Salesman extends Employee
{
    private string $name;
}

class Engineer extends Employee
{
    private string $name;
}
```

## New Code

```php
<?php
class Employee
{
    protected string $name;
}

class Salesman extends Employee
{
    ...
}

class Engineer extends Employee
{
    ...
}
```