# Replace Parameter With Query (324)

Inverse of [Replace Query With Parameter (327)](327_-_Replace_Query_with_Parameter.md)

## Old Code

```php
<?php
availableVacation($anEmployee, $anEmployee->grade);

function availableVacation($anEmployee, $grade)
{
    // Calculate vacation
}
```

## New Code

```php
<?php
availableVacation($anEmployee);

function availableVacation($anEmployee)
{
    $grade = $anEmployee->grade;
    // Calculate vacation
}
```