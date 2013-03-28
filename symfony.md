```
php app/console generate:bundle
```

## Generate getters and setters
```
php app/console generate:doctrine:entities TiendaBundle
```

### Generate entities
```
php app/console doctrine:generate:entity
```

## Database and schema
```
php app/console doctrine:database:create
php app/console doctrine:schema:create    [--dump-sql]
php app/console doctrine:schema:update    [--dump-sql]
```

## Cache
```
php app/console cache:clear
php app/console cache:clear --env=dev	// ==env=prod
```

## Logger
```
$log = $this -> get(‘logger’);
$log -> info(‘Generada en 3 seg’);
```

## Link assets
```
php app/console assets:install [--symlink]
```

## ACL
```
php app/console init:acl
```
