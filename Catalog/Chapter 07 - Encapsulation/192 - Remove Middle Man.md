# Remove Middle Man (192)

Inverse of [Hide Delegate](189%20-%20Hide%20Delegate.md)

## Old Code

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

## New Code

```php
<?php
$manager = aPerson->department->manager;
```