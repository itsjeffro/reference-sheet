# Symfony

## Using persist

Example

```php
$em->persist($entity);

$em->flush();
```

### Updating

When updating an entity, persist is not needed. This is because when an object is queried
Doctrine will know that you would potentially like to save the object.

In this case, you may simply exlude `persist` and call `flush` at the end.
