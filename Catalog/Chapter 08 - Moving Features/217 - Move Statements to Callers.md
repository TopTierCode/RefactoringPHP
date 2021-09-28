# Move Statements to Callers (217)

Inverse of [Move Statements into Function (213)](213%20-%20Move%20Statements%20into%20Function.md)

## Old Code

```php
<?php
emitPhotoData($outStream, $person->photo);
function emitPhotoData($outStream,$photo)
{
    fwrite($outStream,'<p>title: ' . $photo->title . '</p>' . "\n");
    fwrite($outStream,'<p>location: ' . $photo->location . '</p>' . "\n");
}
```

## New Code

```php
<?php
emitPhotoData($outStream, $person->photo);
fwrite($outStream,'<p>location: ' . $person->photo->location . '</p>' . "\n");

function emitPhotoData($outStream,$photo)
{
    fwrite($outStream,'<p>title: ' . $photo->title . '</p>' . "\n");
}
```