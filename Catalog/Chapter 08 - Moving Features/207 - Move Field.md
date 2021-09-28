# Move Function (198)

## Old Code

```php
<?php
class Customer
{
    public function getPlan()
    {
        return $this->plan;
    }
    public function getDiscountRate()
    {
        return $this->discountRate;
    }
}
```

## New Code

```php
<?php
class Customer
{
    public function getPlan()
    {
        return $this->plan;
    }
    public function getDiscountRate()
    {
        return $this->plan->discountRate;
    }
}
```