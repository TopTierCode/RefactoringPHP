# Encapsulate Collection (170)

## Old Code

```php
<?php
class Person
{
    protected $courses;
    public function getCourses()
    {
        return $this->courses;
    }
    
    public function setCourses($aList)
    {
        $this->courses = $aList;
    }
}
```

## New Code

```php
<?php
class Organization
{
    protected $courses;
    public function getCourses()
    {
        return $this->courses;
    }
    
    public function addCourse($aCourse) {
        // add course here
    }
    
    public function removeCourse($aCourse) {
        // remove course here
    }
    
}
```