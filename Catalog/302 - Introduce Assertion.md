# Introduce Assertion (302)

## Old Code
```php
<?php
if ( $this->discountRate ) {
    $base = $base - ($this->discountRate * $base);
}
```

## New Code
```php
<?php
assert($this->discountRate > 0);
if ( $this->discountRate ) {
    $base = $base - ($this->discountRate * $base);
}
```