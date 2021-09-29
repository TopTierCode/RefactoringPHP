# Pull Up Constructor Body (355)

## Old Code

```php
<?php
class Party
{
    ...
}

class Employee extends Party
{
    public function __construct($name, $id, $monthlyCost)
    {
        parent::__construct();
        $this->id = $id;
        $this->name = $name;
        $this->monthlyCost = $monthlyCost;
    }
}
```

## New Code

```php
<?php
class Party
{
    public function __construct($name)
    {
        $this->name = $name;
    }
}

class Employee extends Party
{
    public function __construct($name, $id, $monthlyCost)
    {
        parent::__construct($name);
        $this->id = $id;
        $this->monthlyCost = $monthlyCost;
    }
}
```