# Changing a Parameter to One of Its Properties

## Old Code

```php
<?php
function inNewEngland($aCustomer)
{
    return in_array($aCustomer->address->state,['MA', 'CT', 'ME', 'VT', 'NH', 'RI'],true);   
}
```

## Intermediate Code

Apply [Extract Variable (119)](../119%20-%20Extract%20Variable.md)

```php
<?php
function inNewEngland($aCustomer)
{
    $stateCode = $aCustomer->address->state;
    return in_array($stateCode,['MA', 'CT', 'ME', 'VT', 'NH', 'RI'],true);   
}
```
## Intermediate Code

Apply [Extract Function (106)](../106%20-%20Extract%20Function.md)

```php
<?php
function inNewEngland($aCustomer)
{
    $stateCode = $aCustomer->address->state;
    return xxNEWinNewEngland($stateCode);   
}
function xxNEWinNewEngland($stateCode)
{
    return in_array($stateCode,['MA', 'CT', 'ME', 'VT', 'NH', 'RI'],true);
}
```
## Intermediate Code

Apply [Inline Variable (123)](../123%20-%20Inline%20Variable.md)

```php
<?php
function inNewEngland($aCustomer)
{
    return xxNEWinNewEngland($aCustomer->address->state);   
}
function xxNEWinNewEngland($stateCode)
{
    return in_array($stateCode,['MA', 'CT', 'ME', 'VT', 'NH', 'RI'],true);
}
```

## Intermediate Note
Change all callers using [Inline Function (115)](../115%20-%20Inline%20Function.md), then apply [Renaming a Function](Renaming%20a%20Function%20-%20Simple.md).

## New Code

```php
<?php
function inNewEngland($stateCode)
{
    return in_array($stateCode,['MA', 'CT', 'ME', 'VT', 'NH', 'RI'],true);
}
```