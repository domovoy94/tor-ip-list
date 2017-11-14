# Tor IP List for Composer

## Description

This tiny repository aims to provide an easy solution to get all nodes Tor IP inside your project using composer.

## Install via composer

Just run the following command in your project root :

```
composer require machou/tor-ip-list
```

## Examples

```php
<?php
$ip = $_SERVER['REMOTE_ADDR'];

function is_tor($ip)
{
	return in_array($ip, array_map('trim', file('tor-ip-list/Tor_ip_list_ALL.csv'))) ? true : false;
}


function is_tor_exit($ip)
{
	return in_array($ip, array_map('trim', file('tor-ip-list/Tor_ip_list_EXIT.csv'))) ? true : false;
}
```

## License

The Tor IP databases are distributed under the [The MIT License](https://opensource.org/licenses/MIT).
The attribution requirement may be met by including the following in all advertising and documentation mentioning features of or use of this database:

> This product includes Tor IP List data created by MaxMind, available from <a href="https://torstatus.blutmagie.de/">Tor Network Status</a>.