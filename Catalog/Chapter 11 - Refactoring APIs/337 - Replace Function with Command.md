# Replace Function with Command (337)

Inverse of [Replace Command with Function (344)](344%20-%20Replace%20Command%20with%20Function.md)

## Old Code

```php
<?php
function score($candidate, $medicalExam, $scoringGuide)
{
    $result = 0;
    $healthLevel = 0;
    // long body code
}
```

## New Code

```php
<?php
class Scorer
{
    public function __construct($candidate, $medicalExam, $scoringGuide)
    {
        $this->candidate = $candidate;
        $this->medicalExam = $medicalExam;
        $this->scoringGuide = $scoringGuide;
    }
    
    public function execute()
    {
        $this->result = 0;
        $this->healthLevel = 0;
        // long body code
    }
}
```