# Slide Statements (223)

## Old Code

```php
<?php
$pricingPlan = retrievePricingPlan();
$order = retrieveOrder();
$charge = null;
$chargePerUnit = $pricingPlan->unit;
```

## New Code

```php
<?php
$pricingPlan = retrievePricingPlan();
$chargePerUnit = $pricingPlan->unit;
$order = retrieveOrder();
$charge = null;
```