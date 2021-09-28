# Split Loop (227)

## Old Code

```php
<?php
$averageAge = 0;
$totalSalary = 0;
foreach($people as $p) {
    $averageAge += $p->age;
    $totalSalary += $p->salary;
}

$averageAge = $averageAge / count($people);
```

## New Code

```php
<?php
$totalSalary = 0;
foreach($people as $p) {
    $totalSalary += $p->salary;
}

$averageAge = 0;
foreach($people as $p) {
    $averageAge += $p->age;
}
$averageAge = $averageAge / count($people);
```