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

Apply [Extract Variable (119)](../119_-_Extract_Variable.md)

```php
<?php
function inNewEngland($aCustomer)
{
    $stateCode = $aCustomer->address->state;
    return in_array($stateCode,['MA', 'CT', 'ME', 'VT', 'NH', 'RI'],true);   
}
```
## Intermediate Code

Apply [Extract Function (106)](../106_-_Extract_Function.md)

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

Apply [Inline Variable (123)](../123_-_Inline_Variable.md)

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
Change all callers using [Inline Function (115)](../115_-_Inline_Function.md), then apply [Renaming a Function](Renaming_a_Function_-_Simple.md).

## New Code

```php
<?php
function inNewEngland($stateCode)
{
    return in_array($stateCode,['MA', 'CT', 'ME', 'VT', 'NH', 'RI'],true);
}
```