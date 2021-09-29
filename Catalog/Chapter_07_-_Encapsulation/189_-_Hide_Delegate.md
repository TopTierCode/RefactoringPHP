# Hide Delegate (189)

Inverse of [Remove Middle Man (192)](192_-_Remove_Middle_Man.md)

## Old Code

```php
<?php
$manager = aPerson->department->manager;

```

## New Code

```php
<?php
$manager = $aPerson->getManager();
class Person
{
    public function getManager()
    {
        return $this->department->manager;
    }
}
```