# Install 

## PEAR
```
sudo apt-get install php-pear
sudo pear upgrade PEAR

sudo pear config-set auto_discover 1
sudo pear install pear.phpunit.de/PHPUnit
```

# Composer
```json
{
    ...
    "require-dev": {
        ...
        "phpunit/phpunit": "3.7.*"
        ...
    }
}
```
