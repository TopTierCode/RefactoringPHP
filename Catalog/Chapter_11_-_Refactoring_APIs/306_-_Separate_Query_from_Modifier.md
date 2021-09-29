# Separate Query from Modifier (306)

## Old Code

```php
<?php
function getTotalOutstandingAndSendBill()
{
    $result = array_reduce(
        $customer->invoices,
        function ($total, $each) {
            return $each->amount + $total
        },
        0
    );
    sendBill();
    return $result;
}
```

## New Code

```php
<?php
function totalOutstanding()
{
    return array_reduce(
        $customer->invoices,
        function ($total, $each) {
            return $each->amount + $total
        },
        0
    );
}

function sendBill()
{
    $emailGateway->send(formatBill($customer));
}
```