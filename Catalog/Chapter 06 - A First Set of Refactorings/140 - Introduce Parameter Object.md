# Introduce Parameter Object (140)

## Old Code
```php
<?php
function amountInvoiced($startDate, $endDate) {}
function amountReceived($startDate, $endDate) {}
function amountOverdue($startDate, $endDate) {}
```

## New Code
```php
<?php
function amountInvoiced($aDateRange) {}
function amountReceived($aDateRange) {}
function amountOverdue($aDateRange) {}
```