# Split Variable (240)

## Old Code

```php
<?php
$temp = 2 * ($height + $width);
echo $temp. "\n";
$temp = $height * $width;
echo $temp . "\n";
```

## New Code

```php
<?php
$perimeter = 2 * ($height + $width);
echo $perimeter. "\n";
$area = $height * $width;
echo $area . "\n";
```