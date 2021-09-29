# Substitute Algorithm (195)

## Old Code

```php
<?php
function foundPerson($people) {
    for ( $i = 0; $i < count($people); $i++ ) {
        if ( $people[$i] === 'Don' ) {
            return 'Don';
        }
        if ( $people[$i] === 'John' ) {
            return 'John';
        }
        if ( $people[$i] === 'Kent' ) {
            return 'Kent';
        }
       
    }
    return '';
}
```

## New Code

```php
<?php
function foundPerson($people) {
    $candidates = ['Don','John', 'Kent'];
    $intersect = array_intersect($people,$candidates);
    return array_shift($intersect) ?? '';
}
```