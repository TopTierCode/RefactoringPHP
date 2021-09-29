# Replace Conditional with Polymorphism (272)

## Old Code

```php
<?php
switch ( $bird->type ) {
    case 'EuropeanSwallow':
        return 'average';
    case 'AfricanSwallow':
        return $bird->numberOfCoconuts > 2 ? 'tired' : 'average';
    case 'NorwegianBlueParrot':
        return $bird->voltage > 100 ? 'scorched' : 'beautiful';
    default:
        return 'unknown';
}
```

## New Code

```php
<?php
class EuropeanSwallow
{
    public function getPlumage()
    {
        return 'average';
    }
}

class AfricanSwallow
{
    public function getPlumage()
    {
        return $this->numberOfCoconuts > 2 ? 'tired' : 'average';
    }
}

class NorwegianBlueParrot
{
    public function getPlumage()
    {
        return $this->voltage > 100 ? 'scorched' : 'beautiful';
    }
}
```