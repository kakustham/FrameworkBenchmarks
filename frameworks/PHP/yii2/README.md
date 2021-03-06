# Yii2 Benchmarking Test

This is the Yii2 portion of a [benchmarking test suite](../) comparing a variety of web development platforms.

This uses PHP's composer for dependency resolution. Note 
that [issue 5083](https://github.com/yiisoft/yii2/issues/5083)
affects the `composer.json` file defined here (also see 
[this](https://github.com/francoispluchino/composer-asset-plugin/issues/29) and [this](https://stackoverflow.com/questions/25882271/cannot-update-yii2-via-composer-bower-asset-jquery-could-not-be-found))

### JSON Encoding Test
Uses the PHP standard [JSON encoder](http://www.php.net/manual/en/function.json-encode.php).

* [JSON test controller](app/controllers/SiteController.php)


### Data-Store/Database Mapping Test
Uses the Yii2 Fluent Query Builder.

* [DB test controller](app/controllers/SiteController.php)

### Template Test
Uses Php template

* [Template test controller](application/controllers/Bench.php)


## Infrastructure Software Versions
The tests were run with:

* [Yii2 Version 2](http://yiiframework.com/)
* [PHP Version 5.4.*](http://www.php.net/) with FPM and APC
* [nginx 1.4.0](http://nginx.org/)
* [MySQL 5.5.29](https://dev.mysql.com/)

## Test URLs
### JSON Encoding Test

http://localhost/site/json

### Data-Store/Database Mapping Test

http://localhost/site/db

### Variable Query Test
    
http://localhost/site/db?queries=2

### Templating Test

http://localhost/site/fortunes

### Update Test

http://localhost/site/updates?queries=2

### Plain Text Test

http://localhost/site/plaintext
