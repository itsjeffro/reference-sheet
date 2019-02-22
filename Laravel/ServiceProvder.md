## Boot
- loaded on all requests
- cannot be defered
- can use other services

### Example
```
public function boot();
```

## Register
- loaded when needed
- cannot be used with other services as they may not be loaded
- can be deferred

### Example
```
public function register();
```

## Bindings
- singleton
- bind
- instance