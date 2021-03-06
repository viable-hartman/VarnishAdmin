## VarnishAdmin PHP Library

VarnishAdmin is a PHP Library for manage Varnish reverse proxy cache commands using PHP


## Requirements

VarnishAdmin is supported on PHP 5.6.* and up.


## Instalation

To install this package, run the command below and you will get the latest version
```
composer require jeslopcru/varnishadmin
```

or include this in your composer.json
```
{
  "require": {
    "jeslopcru/varnishadmin": "dev-master"
  }
}
```


## Use
It's very easy to use VarnishAdmin. If you have any question please open an issue 

### Varnish 5
```php
  $varnish = new VarnishAdminSocket('192.168.10.10', 6082, '5.0.0');
  $varnish->purgeUrl('example.com');
  $varnish->quit();
```

### Varnish 4
```php
  $varnish = new VarnishAdminSocket('192.168.10.10', 6082, '4.0.3');
  $varnish->purgeUrl('example.com');
  $varnish->quit();
```

### Varnish 3
```php
  //purge postId  (id = 354)
  //www.example.com?id=354
  $varnish = new VarnishAdminSocket();
  $varnish->purgeUrl('id=354');
  $varnish->quit();
```


# Pull Request
Pull request are welcome using PSR-2, all issues are welcomed

## License
The whole VarnishAdmin package, is released under the MIT license, see LICENSE.

You can use this repo for Docker: https://github.com/newsdev/docker-varnish

Based on [timwhitlock/php-varnish](https://github.com/timwhitlock/php-varnish)

