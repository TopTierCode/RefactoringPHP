# Extract Function (106)

Inverse of [Inline Function (115)](115%20-%20Inline%20Function.md)

## Old Code

```php
<?php
function printOwing($invoice)
{
    printBanner();
    $outstanding = calculateOutstanding();
    
    // print details
    echo "name: {$invoice->customer}\n";
    echo "amount: {$outstanding}\n";
}
```

## New Code

```php
<?php
function printOwing($invoice)
{
    printBanner();
    $outstanding = calculateOutstanding();
    printDetails($invoice,$outstanding);
}

function printDetails($invoice,$outstanding)
{    
    // print details
    echo "name: {$invoice->customer}\n";
    echo "amount: {$outstanding}\n";
}
```
