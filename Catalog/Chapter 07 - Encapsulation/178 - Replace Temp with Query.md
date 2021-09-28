# Replace Temp With Query (178)

## Old Code

```php
<?php
$basePrice = $this->quantity * $this->itemPrice;
if ( $basePrice > 1000 ) {
    return $basePrice * 0.95;
} else {
    return $basePrice * 0.98;
}
```

## New Code

```php
<?php
public function basePrice()
{ 
    return $this->quantity * $this->itemPrice;
}
...
if ( $this->basePrice() > 1000 ) {
    return $this->basePrice() * 0.95;
} else {
    return $this->basePrice() * 0.98;
}
```