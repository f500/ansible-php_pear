php_pear
========

Install pear

Requirements
------------

Debian Wheezy with the package python-pycurl and python-software-properties installed.

Role Variables
--------------

```
php_pear_channels: []
php_pear_libraries: []
```

**Example channels and libraries**

```
php_pear_channels:
  - pear.symfony.com
php_pear_libraries:
  - PHP_CodeSniffer
```

Dependencies
------------

Depends on f500.php, f500.php_cli.

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - { role: f500.php_pear }

Faq
---
If the `pear` command fails because of deprecation warnings change the f500.php_cli role to the following:

    roles:
        - { role: f500.php_cli, php_cli_error_reporting: 'E_ALL & ~E_DEPRECATED' }
        - { role: f500.php_pear }

License
-------

LGPL

Author Information
------------------

Jasper N. Brouwer, jasper@nerdsweide.nl

Ramon de la Fuente, ramon@delafuente.nl
