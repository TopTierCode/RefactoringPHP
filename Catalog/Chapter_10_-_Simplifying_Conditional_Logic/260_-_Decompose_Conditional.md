# Decompose Conditional (260)

## Old Code

```php
<?php
if ( !$aDate->isBefore($plan->summerStart) && !$aDate->isAfter($plan->summerEnd) {
    $charge = $quantity * $plan->summerRate;
} else {
    $charge = $quantity * $plan->regularRate + $plan->regularServiceCharge;
}
```

## New Code

```php
<?php
if ( summer() ) {
    $charge = summerCharge();
} else {
    $charge = regularCharge();
}
```