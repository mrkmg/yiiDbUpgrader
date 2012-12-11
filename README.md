yiiDbUpgrader
=============

Yii DbUpgrader Component can be used to automate upgrading a database to a new version(s).

Installation
============

Copy `DbUpgrader.php` to `protected/components/`

Usage
=====

- Create a folder in your Yii data folder (`protected/data`) called `dbversion`.
- Each time you make changes to the database, place the sql code for those changes into numbered sql files in that directory. The follow are both valid:

```
1.sql
2.sql
3.sql
4.sql
```

```
001.sql
002.sql
003.sql
004.sql
```

- Somewhere in your code, you can run the following to actually perform the check and upgrade.

```php
$dbu = new DbUpgrader;
$dbu->runUpgrade();
```

- If you want a verbose output (useful for cli access and logging)

```php
$dbu = new DbUpgrader;
$dbu->runUpgrade(true);
```
