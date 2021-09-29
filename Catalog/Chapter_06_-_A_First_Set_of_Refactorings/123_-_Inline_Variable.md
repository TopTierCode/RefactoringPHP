# Inline Function (123)
Inverse of [Extract Variable (119)](119_-_Extract_Variable.md)
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