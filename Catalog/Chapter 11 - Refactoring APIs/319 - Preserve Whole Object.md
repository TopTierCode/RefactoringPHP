# Preserve Whole Object (319)

## Old Code

```php
<?php
$low = $aRoom->daysTempRange->low;
$high = $aRoom->daysTempRange->high;
if ( $aPlan->withinRange($low, $high) ) {
    ...
}
```

## New Code

```php
<?php
if ( $aPlan->withinRange($aRoom->daysTempRange) ) {
    ...
}
```