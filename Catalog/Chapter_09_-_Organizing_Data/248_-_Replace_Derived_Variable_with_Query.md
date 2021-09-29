# Replace Derived Variable with Query (248)

## Old Code

```php
<?php
public function getDiscountedTotal()
{
    return $this->discountedTotal;
}
public function setDiscount($aNumber)
{
    $old = $this->discount;
    $this->discount = $aNumber;
    $this->discountedTotal += $old - $aNumber;
}
```

## New Code

```php
<?php
public function getDiscountedTotal()
{
    return $this->baseTotal - $this->discountedTotal;
}
public function setDiscount($aNumber)
{
    $this->discount = $aNumber;
}
```