# Renaming a Function - Migration Mechanics

## Old Code
```php
<?php
function circum($radius)
{
    return 2 * M_PI * $radius; 
}
```
## Intermediate Code
Apply [Extract Function (106)](../106%20-%20Extract%20Function.md)
```php
<?php
function circum($radius)
{
    return circumference($radius);
}
function circumference($radius)
{
    return 2 * M_PI * $radius;
}
```
## New Code
Apply [Inline Function (115)](../115%20-%20Inline%20Function.md)
```php
<?php
function circumference($radius)
{
    return 2 * M_PI * $radius;
}
```