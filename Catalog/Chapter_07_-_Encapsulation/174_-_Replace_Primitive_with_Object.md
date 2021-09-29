# Replace Primitive with Object (174)

_Note: Due to semantic differences between languages, this sample differs more than most._

## Old Code

```php
<?php
array_filter($orders,function($o) {
    return 'high' === $o['priority'] ||
    'rush' === $o['priority']
});
```

## New Code

```php
<?php
array_filter($orders,function($o) {
    return $o['priority']->higherThan(new Priority('normal'));
});
```