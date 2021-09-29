# Replace Superclass with Delegate (399)

_Note: Class is named `ListX` because `List` is a reserved keyword in PHP._

## Old Code

```php
class ListX
{
    ...
}

class Stack extends ListX
{
    ...
}
```

## New Code

```php
<?php
class Stack
{
    public function __construct()
    {
        $this->storage = new ListX();
    }
}
class ListX
{
    ...
}
```