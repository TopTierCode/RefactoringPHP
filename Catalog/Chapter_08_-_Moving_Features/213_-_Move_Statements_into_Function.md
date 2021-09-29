# Move Statements into Function (213)

Inverse of [Move Statements to Callers (217)](217_-_Move_Statements_to_Callers.md)

## Old Code

```php
<?php
array_push($result,'<p>title: ' . $person->photo->title . '</p>');
$result = array_merge($result,photoData($person->photo));

function photoData($aPhoto)
{
    return [
        '<p>location: ' . $aPhoto->location . '</p>',
        '<p>date: ' . $aPhoto->date->toDateString() . '</p>',    
    ];
}
```

## New Code

```php
<?php
$result = array_merge($result,photoData($person->photo));

function photoData($aPhoto)
{
    return [
        '<p>title: ' . $person->photo->title . '</p>',
        '<p>location: ' . $aPhoto->location . '</p>',
        '<p>date: ' . $aPhoto->date->toDateString() . '</p>',    
    ];
}
```