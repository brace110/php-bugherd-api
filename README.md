# PHP Bugherd API

A simple Object Oriented wrapper for Bugherd API, written with PHP5.

Uses [Bugherd API](https://www.bugherd.com/api_v2).

## Features

* Follows PSR-0 conventions and coding standard: autoload friendly
* API entry points implementation state :
 * *OK Organizations
 * *OK Projects
 * *NOK Users
 * *NOK Tasks
 * *NOK Comments
 * *NOK Webhooks


## Todo



## Requirements

* PHP >= 5.3.2 with [cURL](http://php.net/manual/en/book.curl.php) extension,
* An Account to bugherd then obtain your *API access key* in Settings > General Settings.

## Install

Through [composer](http://getcomposer.org/download/), simply run :

```bash
$ php composer.phar require beleneglorion/php-bugherd-api:dev-master
```

## Basic usage of `php-bugherd-api` client

```php
<?php

// This file is generated by Composer
require_once 'vendor/autoload.php';

$client = new Bugherd\Client('API_ACCESS_KEY');

$client->api('user')->all();
$client->api('user')->listing();

$client->api('task')->create('project_id',array(
   'description'=>'Example task',
   'priority'=>'normal',
   'status'=>'backlog',
   'requester_id'=>123,
   'tag_names'=>array('ui','feature'),
   'assigned_to_id'=>123,
   'external_id'=>'ABC123'
));

```


### Thanks!

- Thanks to [Kevin Saliou](https://github.com/kbsali/) for the php-redmine-api library, great source of inspiration!
