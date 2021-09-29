# Replace Query With Parameter (327)

Inverse of [Replace Parameter With Query (324)](324%20-%20Replace%20Parameter%20with%20Query.md)

## Old Code

```php
<?php
targetTemperature($aPlan);

function targetTemperature($aPlan)
{
    ...
    $currentTemperature = $thermostat->currentTemperature;
    // rest of function
}
```

## New Code

```php
<?php
targetTemperature($aPlan, $thermostat->currentTemperature);

function targetTemperature($aPlan, $currentTemperature)
{
    // rest of function
}
```