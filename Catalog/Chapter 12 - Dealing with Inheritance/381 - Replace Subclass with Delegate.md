# Replace Subclass with Delegate (381)

## Old Code

```php
class Order
{
    public function getDaysToShip
    {
        return $this->warehouse->daysToShip;
    }
}

class PriorityOrder extends Order
{
    public function getDaysToShip
    {
        return $this->priorityPlan->daysToShip;
    }
}
```

## New Code

```php
<?php
class Order
{
    public function getDaysToShip
    {
        return $this->priorityDelegate ?
            $this->priorityDelegate->daysToShip() :
            $this->warehouse->daysToShip;
    }
}

class PriorityOrderDelegate
{
    public function getDaysToShip
    {
        return $this->priorityPlan->daysToShip;
    }
}
```