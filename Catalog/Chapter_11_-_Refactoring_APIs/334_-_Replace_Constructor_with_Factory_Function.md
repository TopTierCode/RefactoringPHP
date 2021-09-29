# Replace Constructor with Factory Function (334)

## Old Code

```php
<?php
$leadEngineer = new Employee($document->leadEngineer, 'E');
```

## New Code

```php
<?php
$leadEngineer = createEngineer($document->leadEngineer);
```