# Combine Functions Into Transform (149)

## Old Code
```php
<?php
function base($aReading){}
function taxableCharge($aReading){}
```

## New Code
```php
<?php
function enrichReading($argReading) {
    $aReading = clone $argReading;
    $aReading->baseCharge = base($aReading);
    $aReading->taxableCharge = taxableCharge($aReading);
    return $aReading;    
}
```