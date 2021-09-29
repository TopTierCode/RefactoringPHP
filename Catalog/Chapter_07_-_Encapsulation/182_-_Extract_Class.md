# Extract Class (182)

Inverse of [Inline Class (186)](186_-_Inline_Class.md)

## Old Code

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

## New Code

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