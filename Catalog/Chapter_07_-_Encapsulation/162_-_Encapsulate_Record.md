# Encapsulate Record (162)

## Old Code

```php
<?php
$organization = [
    'name' => 'Acme Gooseberries',
    'country' => 'GB'
];
```

## New Code

```php
<?php
class Organization
{
    protected $name;
    protected $country;
    public function __construct($data)
    {
        $this->name = $data->name;
        $this->country = $data->country;
    }
    
    public function getName()
    {
        return $this->name;
    }
    
    public function setName($arg)
    {
        $this->name = $arg;
    }
    
    public function getCountry()
    {
        return $this->country;
    }
    
    public function setCountry($arg)
    {
        $this->country = $arg;
    }
    
}
```