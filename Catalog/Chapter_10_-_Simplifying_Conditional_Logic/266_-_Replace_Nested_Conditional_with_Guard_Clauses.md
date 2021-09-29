# Replace Nested Conditional with Guard Clauses (266)

## Old Code

```php
<?php
function getPayAmount()
{
    ...
    $result = null;
    if ( $isDead ) {
        $result = deadAmount();
    } else {
        if ( $isSeparated ) {
            $result = separatedAmount();
        } else {
            if ( $isRetired ) {
                $result = retiredAmount();
            } else {
                $result = normalPayAmount();
            }
        }
    }
    return $result;
}
```

## New Code

```php
<?php
function getPayAmount()
{
    ...
    if ( $isDead ) {
        return deadAmount();
    }
    if ( $isSeparated ) {
        return separatedAmount();
    }
    if ( $isRetired ) {
        return retiredAmount();
    }
    return $normalPayAmount();
}
```