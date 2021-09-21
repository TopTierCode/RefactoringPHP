# Inline Function
Inverse of [Extract Variable (119)](119%20-%20Extract%20Variable.md)
## Old Code
```php
<?php
$basePrice = $anOrder->basePrice;
return ($basePrice > 1000);
```

## New Code
```php
<?php
return ($anOrder->basePrice > 1000);
```