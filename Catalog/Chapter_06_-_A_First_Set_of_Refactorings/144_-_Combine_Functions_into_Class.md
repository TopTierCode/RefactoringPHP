# Combine Functions Into Class (144)

## Old Code

```php
<?php
function base($aReading){}
function taxableCharge($aReading){}
function calculateBaseCharge($aReading){}
```

## New Code

```php
<?php
class Reading
{
    function base(){}
    function taxableCharge(){}
    function calculateBaseCharge(){}
}
```