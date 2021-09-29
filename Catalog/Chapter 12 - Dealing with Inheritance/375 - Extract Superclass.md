# Extract Superclass (375)

## Old Code

```php
class Department
{
    public function getTotalAnnualCost()
    {
        ...
    }
    
    public function getName()
    {
        ...
    }
    
    public function getHeadCount()
    {
        ...
    }
}

class Employee
{
    public function getAnnualCost()
    {
        ...
    }
    
    public function getName()
    {
        ...
    }
    
    public function getId()
    {
        ...
    }
   
}
```

## New Code

```php
<?php
class Party
{
    public function getName()
    {
        ...
    }
    
    public function getAnnualCost()
    {
        ...
    }
    
}
class Department extends Party
{
    public function getAnnualCost()
    {
        ...
    }
    
    public function getHeadCount()
    {
        ...
    }
}

class Employee extends Party
{
    public function getAnnualCost()
    {
        ...
    }
    
    public function getId()
    {
        ...
    }
   
}
```