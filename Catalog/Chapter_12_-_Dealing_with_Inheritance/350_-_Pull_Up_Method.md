# Pull Up Method (350)

Inverse of [Push Down Method (359)](359_-_Push_Down_Method.md)

## Old Code

```php
<?php
class Employee
{
    ...
}

class Salesman extends Employee
{
    public function getName()
    {
        ...
    }
}

class Engineer extends Employee
{
    public function getName()
    {
        ...
    }
}
```

## New Code

```php
<?php
class Employee
{
    public function getName()
    {
        ...
    }
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