# Change Value to Reference (256)

Inverse of [Change Reference to Value (252)](252%20-%20Change%20Reference%20to%20Value.md)

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