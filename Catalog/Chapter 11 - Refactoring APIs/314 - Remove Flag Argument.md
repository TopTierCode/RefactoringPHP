# Remove Flag Argument (314)

## Old Code

```php
<?php
public function setDimension($name, $value)
{
    if ( $name === 'height' ) {
        $this->height = $value;
        return;
    }
    if ( $name === 'width' ) {
        $this->width = $value;
        return;
    }
}
```

## New Code

```php
<?php
public function setHeight($value)
{
    $this->height = $value;
}

public function setWidth($value)
{
    $this->width = $value;
}
```