# Remove Subclass (369)

Inverse of [Replace Type Code with Subclasses (362)](362%20-%20Replace%20Type%20Code%20with%20Subclasses.md)

## Old Code

```php
<?php
class Person {
    public function getGenderCode()
    {
        return 'X';
    }
}

class Male extends Person {
    public function getGenderCode()
    {
        return 'M';
    }
}

class Female extends Person {
    public function getGenderCode()
    {
        return 'F';
    }
}
```

## New Code

```php
<?php
class Person {
    public function getGenderCode()
    {
        return $this->genderCode;
    }
}
```