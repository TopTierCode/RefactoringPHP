# Encapsulate Variable (132)
_Note: this refactor has more details in this version to convey the ideas in a PHP-Centered manner._
## Old Code
```php
<?php
class Book
{
    public $defaultOwner = ['firstName' => 'Martin', 'lastName' => 'Fowler'];
}
```

## New Code
```php
<?php
class Book
{
    protected $defaultOwner = ['firstName' => 'Martin', 'lastName' => 'Fowler'];
    public function getDefaultOwner()
    {
        return $this->defaultOwner;
    }
    
    public function setDefaultOwner($arg)
    {
        $this->defaultOwner = $arg;
    }
}
```