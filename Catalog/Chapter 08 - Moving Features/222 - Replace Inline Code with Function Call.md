# Replace Inline Code with Function Call (222)

## Old Code

```php
<?php
$appliesToMass = false;
foreach($states as $s) {
    if ( $s === 'MA' ) {
        $appliesToMass = true;
    }
}
```

## New Code

```php
<?php
$appliesToMass = in_array('MA',$states);
```