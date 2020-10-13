
# Symfony
## Clear cache
```rm -rf var/cache/*```
## Behat test
```php vendor/bin/behat  PATHTOTEST```
## Unit test 
### Test name
```php vendor/bin/phpunit --filter {tesName}```
### File Name
```php vendor/bin/phpunit --filter {src/.../file.php} ```
### Stop on failure
```php vendor/bin/phpunit --stop-on-failure```

## CS Fixer
```php vendor/bin/php-cs-fixer```
