# Phalcon Devtools

[![Latest Version](https://img.shields.io/packagist/v/phalcon/devtools.svg?style=flat-square)][:devtools:]
[![Software License](https://img.shields.io/badge/license-BSD--3-brightgreen.svg?style=flat-square)][:license:]
[![Total Downloads](https://img.shields.io/packagist/dt/phalcon/devtools.svg?style=flat-square)][:packagist:]
[![Daily Downloads](https://img.shields.io/packagist/dd/phalcon/devtools.svg?style=flat-square)][:packagist:]
[![Build Status](https://travis-ci.org/phalcon/phalcon-devtools.svg?branch=master)][:travis:]

![Phalcon WebTools](https://cloud.githubusercontent.com/assets/1256298/18617851/b7d31558-7de2-11e6-83e0-30e5902af714.png)


## What's Phalcon?

Phalcon PHP is a web framework delivered as a C extension providing high performance and lower resource consumption.

## What are Devtools?

This tools provide you useful scripts to generate code helping to develop faster and easy applications that use
with Phalcon framework.

## Requirements

* PHP >= 5.5
* Phalcon >= 3.0.0

## Installing via Composer

Install composer in a common location or in your project:

```bash
curl -s http://getcomposer.org/installer | php
```

Create the composer.json file as follows:

```json
{
    "require-dev": {
        "phalcon/devtools": "~3.0"
    }
}
```

If you are still using Phalcon 2.0.x, create a `composer.json` with the following instead:

```json
{
    "require-dev": {
        "phalcon/devtools": "^2.0"
    }
}
```

Run the composer installer:

```bash
php composer.phar install
```

## Build `.phar`

Install composer and box in a common location or in your project:
```bash
curl -s http://getcomposer.org/installer | php
bin/composer install
```

Build phar file `phalcon-devtools`
```bash
bin/box build -v
chmod +xr ./phalcon.phar
# Test it!
php ./phalcon.phar
```

## Installation via Git

Phalcon Devtools can be installed by using Git.

Just clone the repo and checkout the current branch:

```bash
cd ~
git clone https://github.com/phalcon/phalcon-devtools.git
cd phalcon-devtools
```

This method requires a little bit more of setup. Probably the best way would be to symlink
the `phalcon.php` to a directory in your `PATH`, so you can issue phalcon commands in each directory
where a phalcon project resides.

```bash
ln -s ~/phalcon-devtools/phalcon.php /usr/bin/phalcon
chmod ugo+x /usr/bin/phalcon
```

If you get a `"phalcon: command not found"` message while creating the symlink, make an alias.

```bash
alias phalcon=/home/[USERNAME]/phalcon-devtools/phalcon.php
```

## Usage

To get a list of available commands just execute following:

```bash
phalcon commands help
```

This command should display something similar to:

```sh
$ phalcon --help

Phalcon DevTools (3.0.4)

Help:
  Lists the commands available in Phalcon devtools

Available commands:
  info             (alias of: i)
  commands         (alias of: list, enumerate)
  controller       (alias of: create-controller)
  module           (alias of: create-module)
  model            (alias of: create-model)
  all-models       (alias of: create-all-models)
  project          (alias of: create-project)
  scaffold         (alias of: create-scaffold)
  migration        (alias of: create-migration)
  webtools         (alias of: create-webtools)
```

## Database adapter

Should add `adapter` parameter in your `db` config file (if you use not MySQL database).

For PostgreSQL it will be something like:

```php
$config = [
  'host'     => 'localhost',
  'dbname'   => 'my_db_name',
  'username' => 'my_db_user',
  'password' => 'my_db_user_password',
  'adapter'  => 'Postgresql'
];
```

## License

Phalcon Developer Tools is open source software licensed under the [New BSD License][:license:].<br>
© Phalcon Framework Team and contributors

[:packagist:]: https://packagist.org/packages/phalcon/devtools
[:devtools:]: https://github.com/phalcon/phalcon-devtools
[:license:]: https://github.com/phalcon/phalcon-devtools/blob/master/LICENSE.txt
[:travis:]: https://travis-ci.org/phalcon/phalcon-devtools
