# Change Reference to Value (252)

Inverse of [Change Value to Reference (256)](256%20-%20Change%20Value%20to%20Reference.md)

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