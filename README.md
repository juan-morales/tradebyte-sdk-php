# Tradebyte SDK

SDK to handle all different ways to interact with Tradebyte API. more infromations you will find on [TB.IO](https://tradebyte.io/).

#### !!! this repository is in WIP state !!!

## Features

* the sdk is build that way that it not consume much memory and can even process gigabyte of data. this is done by using iterators and xml readers.
* you can choose between on the fly processing or on downloading it first and reprocessing it later.
* the following data end-points are implemented

- [x] order list (on the fly)
- [x] order list (download/open)
- [x] order ack
- [ ] product list (on the fly)
- [ ] product list (download/open)
- [ ] import push
- [x] stock list (on the fly)
- [ ] stock list (download/open)
- [ ] message list
- [ ] message ack

## Requirements

* credentials (username,password,account-number)
  * see https://tb-io.tradebyte.org/how-to/generate-rest-api-credentials-in-tb-one/
* PHP >= 7.3
* Composer

## Install

1. download composer (https://getcomposer.org/download)
2. execute the following:

```bash
$ composer require kinimodmeyer/tradebyte-sdk:dev-main
```

## Execute Examples

copy ``vendor/kinimodmeyer/tradebyte-sdk/examples/`` folder to your project-root.
rename ``examples/example_credentials.php`` to ``examples/credentials.php`` and replace the credentials.
execute the examples from the cli:

```bash
$ php examples/products.php channel=1370 id=123
$ php examples/orders.php channel=1370 id=123
$ php examples/stock.php channel=1370 delta=123
```
