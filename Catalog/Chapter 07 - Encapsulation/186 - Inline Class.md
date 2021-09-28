# Inline Class (186)

Inverse of [Extract Class (182)](182%20-%20Extract%20Class.md)

## Old Code

```php
<?php
class Person
{
    public function getOfficeAreaCode()
    {
        return $this->telephoneNumber->officeAreaCode;
    }
    
    public function getOfficeNumber()
    {
        return $this->telephoneNumber->officeNumber;
    }
}
class TelephoneNumber
{
    public function getAreaCode()
    {
        return $this->areaCode;
    }
    
    public function getNumber()
    {
        return $this->number;
    }
}
```

## New Code

```php
<?php
class Person
{
    public function getOfficeAreaCode()
    {
        return $this->officeAreaCode;
    }
    
    public function getOfficeNumber()
    {
        return $this->officeNumber;
    }
}
```