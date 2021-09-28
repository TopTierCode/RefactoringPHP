# Adding a Parameter

## Old Code

```php
<?php
class Book
{
    function addReservation($customer)
    {
        $this->_reservations[] = $customer;    
    }
}
```

## Intermediate Code

Apply [Extract Function (106)](../106%20-%20Extract%20Function.md)

```php
<?php
class Book
{
    function addReservation($customer)
    {
        $this->zz_addReservation($customer);    
    }
    
    function zz_addReservation($customer)
    {
        $this->_reservations[] = $customer;
    }
}
```

## Intermediate Code

Add parameter to new declaration and its call.

```php
<?php
class Book
{
    function addReservation($customer)
    {
        $this->zz_addReservation($customer, false);    
    }
    
    function zz_addReservation($customer, $isPriority)
    {
        $this->_reservations[] = $customer;
    }
}
```

## Intermediate Code

Apply [Introduce Assertion (302)](../302%20-%20Introduce%20Assertion.md)

```php
<?php
class Book
{
    function addReservation($customer)
    {
        $this->zz_addReservation($customer, false);    
    }
    
    function zz_addReservation($customer, $isPriority)
    {
        // Note: this can be made unnecessary by simply type hinting the property.
        assert($isPriority === true || $isPriority === false);
        $this->_reservations[] = $customer;
    }
}
```

## Intermediate Note
Change all callers using [Inline Function (115)](../115%20-%20Inline%20Function.md), then apply [Renaming a Function](Renaming%20a%20Function%20-%20Simple.md).

## New Code

```php
<?php
class Book
{
    function addReservation($customer, $isPriority)
    {
        $this->_reservations[] = $customer;
    }
}
```