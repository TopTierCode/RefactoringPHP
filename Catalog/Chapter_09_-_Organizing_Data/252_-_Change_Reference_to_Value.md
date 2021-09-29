# Change Reference to Value (252)

Inverse of [Change Value to Reference (256)](256_-_Change_Value_to_Reference.md)

## Old Code

```php
<?php
class Product {
    public function applyDiscount($arg)
    {
        $this->price->amount -= $arg;
    }
}
```

## New Code

```php
<?php
class Product {
    public function applyDiscount($arg)
    {
        $this->price = new Money($this->price->amount - $arg, $this->price->currency);
    }
}
```