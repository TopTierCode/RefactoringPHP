# Inline Function
Inverse of [Extract Function (106)](106%20-%20Extract%20Function.md)
## Old Code
```php
<?php
function getRating($driver)
{
    return moreThanFiveLateDeliveries($driver) ? 2 : 1;
}

function moreThanFiveLateDeliveries($driver) 
{
    return $driver->numberOfLateDeliveries > 5;
}
```

## New Code
```php
<?php
function getRating($driver)
{
    return ($driver->numberOfLateDeliveries > 5) ? 2 : 1;
}
```