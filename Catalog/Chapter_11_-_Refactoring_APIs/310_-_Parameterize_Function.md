# Parameterize Function (310)

## Old Code

```php
<?php
function tenPercentRaise($aPerson)
{
    $aPerson->salary = $aPerson->salary->multiply(1.1);
}

function fivePercentRaise($aPerson)
{
    $aPerson->salary = $aPerson->salary->multiply(1.05);
}
```

## New Code

```php
<?php
function raise($aPerson, $factor)
{
    $aPerson->salary = $aPerson->salary->multiply(1 + $factor);
}
```