# Change Value to Reference (256)

Inverse of [Change Reference to Value (252)](252_-_Change_Reference_to_Value.md)

## Old Code

```php
<?php
$customer = new Customer($customerData);
```

## New Code

```php
<?php
$customer = $customerRepository->get($customerData->id);
```