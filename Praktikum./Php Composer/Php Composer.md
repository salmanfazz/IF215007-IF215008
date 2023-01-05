## Hello World Package for PHP Composer 

Untuk mengenai penjelasan dokumentasi lebih lanjut dapat mengunjungi [klik link disini](https://packagist.org/packages/ehime/hello-world)
## Usage ##

```bash
$ composer require Salman/hello-world
$ touch test.php
```

```php
<?php
require_once "vendor/autoload.php";

$hello = new Salman\Demo\Hello();
echo $hello->hello();
```

```bash
$ php test.php
```

It will print "Hello World!" then exit.
