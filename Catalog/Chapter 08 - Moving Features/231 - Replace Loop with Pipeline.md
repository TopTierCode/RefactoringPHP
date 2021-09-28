# Replace Loop with Pipeline (231)

_Note: Due to semantic differences between languages, this sample differs more than most._

## Old Code

```php
<?php
$names = [];

foreach($input as $i) {
    if ( $i->job === 'programmer') {
        $names[] = $i->name;
    }
}

```

## New Code

```php
<?php
$names = array_map(
    function ($i) {
        return $i['name'];
    },
    array_filter($input, function ($i) {
        return $i['job'] === 'programmer';
    })
);

```