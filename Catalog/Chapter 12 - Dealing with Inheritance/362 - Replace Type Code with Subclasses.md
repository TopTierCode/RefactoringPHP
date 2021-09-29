# Replace Type Code with Subclasses (362)

Inverse of [Remove Subclass (369)](369%20-%20Remove%20Subclass.md)

## Old Code

```php
<?php
function createEmployee($name, $type)
{
    return new Employee($name, $type);
}
```

## New Code

```php
<?php
function createEmployee($name, $type)
{
    switch ($type) {
        case 'engineer':
            return new Engineer($name);
        case 'salesman':
            return new Salesman($name);
        case 'manager':
            return new Manager($name);
    }
}
```