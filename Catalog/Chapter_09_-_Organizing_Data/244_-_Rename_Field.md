# Rename Field (244)

## Old Code

```php
<?php
class Organization
{
    protected $name;
    public function getName()
    {
        return $this->name;
    }
}
```

## New Code

```php
<?php
class Organization
{
    protected $title;
    public function getTitle()
    {
        return $this->title;
    }
}
```