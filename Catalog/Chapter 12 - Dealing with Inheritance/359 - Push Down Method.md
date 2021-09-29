# Push Down Method (359)

Inverse of [Pull Up Method (350)](350%20-%20Pull%20Up%20Method.md)

## Old Code

```php
<?php
class Employee
{
    public function getQuota()
    {
        ...
    }
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
    public function getQuota()
    {
        ...
    }
}
```