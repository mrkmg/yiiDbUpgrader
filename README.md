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


License
=======

The MIT License (MIT)
Copyright (c) 2013 MrKMG

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
