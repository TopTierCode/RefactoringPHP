# Replace Command with Function (344)

Inverse of [Replace Function with Command (337)](337%20-%20Replace%20Function%20with%20Command.md)

## Old Code

```php
<?php
class ChargeCalculator
{
    public function __construct($customer, $usage)
    {
        $this->customer = $customer;
        $this->usage = $usage;
    }
    
    public function execute()
    {
        return $this->customer->rate * $this->usage;
    }
}
```

## New Code

```php
<?php
function charge($customer, $usage)
{
    return $customer->rate * $usage;
}
```