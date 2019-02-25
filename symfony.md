
# Symfony

## Clear cache
```
rm -rf var/cache/*
```
## Behat test
php vendor/bin/behat  PATHTOTEST
## Unit test 
php vendor/bin/phpunit --filter {tesName}
## CS Fixer
php vendor/bin/php-cs-fixer
