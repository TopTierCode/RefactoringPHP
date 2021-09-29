# Split Phase (154)

## Old Code

```php
<?php
$orderData = preg_split('/\s+/', $orderString, -1, PREG_SPLIT_NO_EMPTY);
[$junk,$priceData] = explode('-',$orderData[0]);
$productPrice = $priceList[$priceData];
$orderPrice = (int)$orderData[1] * $productPrice;
```

## New Code

```php
<?php
$orderRecord = parseOrder($order);
$orderPrice = price($orderRecord,$priceList);

function parseOrder($aString) {
    $values = preg_split('/\s+/', $orderString, -1, PREG_SPLIT_NO_EMPTY);
    [$junk,$productId] = explode('-',$values[0]);
    return [
        'productId' => $productId,
        'quantity' => (int)$values[1]    
    ];
}
function price($order,$priceList) {
    return $order->quantity * $priceList[$order->productId];
}
```