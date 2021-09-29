# Consolidate Conditional Expression (263)

## Old Code

```php
<?php
if ( $anEmployee->seniority < 2 ) {
    return 0;
}
if ( $anEmployee->monthsDisabled > 12 ) {
    return 0;
}
if ( $anEmployee->isPartTime ) {
    return 0;
}
```

## New Code

```php
<?php
if ( isNotEligableForDisability() ) {
    return 0;
}

function isNotEligableForDisablity()
{
    return $anEmployee->seniority < 2 ||
        $anEmployee->monthsDisabled > 12 ||
        $anEmployee->isPartTime;
}
```