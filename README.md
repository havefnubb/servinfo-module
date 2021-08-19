Servinfo module
==============

This is a module for Jelix, displaying system data about the current server into 
a master_admin interface.
It displays on the dashboard following informations (if the user has the right to see them)  :

- server loads
- name of the PHP cache engine
- the database server used into the application
- the database size and number of records
- the PHP version
- others informations given by modules listening the event `servinfoGetInfo`

This module is for Jelix 1.7.2 and higher.

It was originally developped into the [Havefnubb project](https://github.com/havefnubb/havefnubb/).

Setting up the module
=====================

The best method is to use Composer.

In a commande line inside your project, execute:

```
composer require "havefnubb/servinfo-module"
```

Launch the configurator for your application to enable the module

```bash
php dev.php module:configure servinfo
```

After configuring the module, you should launch the installer of your application
to activate the module:

```bash
php install/installer.php
```

Go into the administration of your application, then into the rights
management. Enable the right "Access to server informations" for users
or groups that are authorized to see server informations.

Corresponding users should see server informations on the dashboard.
