Web_ZF2_Apigility_Angular
==============================

Project meant to serve as base for projects based on Zend framework, Apigility, and Angular.

Main Components - What is included basically, you don't need to install.
------------
ZF2 Skeleton Application:
https://github.com/zendframework/ZendSkeletonApplication

Apigility:
https://apigility.org/documentation/recipes/apigility-in-an-existing-zf2-application

Additional Apigility Modules Installed:

Documentation:
https://github.com/zfcampus/zf-apigility-documentation

Swagger Documentation:
https://github.com/zfcampus/zf-apigility-documentation-swagger

Angular: version 1.5.5
https://angularjs.org/

Installation
------------

```
git clone https://github.com/NathanHaley/web_ZF2_Apigility_Angular.git /pathToYourProjectRoot

cd /pathToYourProjectRoot
```

Install composer if not already installed.
```
curl -sS https://getcomposer.org/installer | php
```

Create config/autoload/local.php from dist file.
```
cp config/autoload/local.php.dist  config/autoload/local.php
```

Edit the file config/autoload/local.php to replace the empty return array statement with the following configuration.
```
return array(
    'statuslib' => array(
        'array_mapper_path' => 'data/statuslib.php',
    ),
);
```

From the root dir, put in development mode.
```
php public/index.php development enable
```

Run PHP's development server.
```
php -S 0.0.0.0:8888 -ddisplay_errors=0 -t public public/index.php
```

Pages that should be available:
- Main page: http://localhost:8888/
- Apigility Admin: http://localhost:8888/apigility/ui
- Apigility Swagger: http://localhost:8888/apigility/swagger



