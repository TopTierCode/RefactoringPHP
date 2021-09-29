# Extract Variable (119)

Inverse of [Inline Variable (123)](123_-_Inline_Variable.md)

## Old Code

```php
<?php
return $order->quantity * $order->itemPrice - 
       max(0, $order->quantity - 500) * $order->itemPrice * 0.05 + 
       min($order->quantity * $order->itemPrice * 0.1, 100);
```

## New Code

```php
<?php
$basePrice = $order->quantity * $order->itemPrice;
$quantityDiscount = max(0, $order->quantity - 500) * $order->itemPrice * 0.05;
$shipping = min($basePrice * 0.1, 100);
return $basePrice - $quantityDiscount + $shipping;
```