# Introduce Special Case (289)

## Old Code

```php
<?php
if ( $aCustomer === 'unknown' ) {
    $customerName = 'occupant';
}
```

## New Code

```php
<?php
class UnknownCustomer
{
    public function getName()
    {
        return 'occupant';
    }
}
```