Mongator Behaviors [![Build Status](https://travis-ci.org/mongator/behaviors.png?branch=master)](https://travis-ci.org/mongator/behaviors)
==============================

These are the official behaviors of Mongator.

- [Timestampable](doc/06_timestampable.md): saves the creation and/or update date in the documents
- [Ipable](doc/04_ipable.md): saves the IP from where documents are created and/or saved
- [Sluggable](doc/05_sluggable.md): saves the slug of a field in the documents
- [Archivable](doc/01_archivable.md): Save a document copy from one collection to other
- [Tokenizable](doc/07_tokenizable.md): Generate a token on creation
- [Hasable](doc/03_hashable.md): Generate a hash for a given fields/rels/embs from the given document, on update and or creation
- [AutoIncrementable](doc/02_auto_incrementable.md): Auto incrementable field like [AUTO_INCREMENT](http://dev.mysql.com/doc/refman/5.0/en/example-auto-increment.html) at MySQL

Requirements
------------

* PHP 5.3.x;
* mongator/mongator


Installation
------------

The recommended way to install Mongator Behaviors is [through composer](http://getcomposer.org).
You can see [package information on Packagist.](https://packagist.org/packages/mongator/behaviors)

```JSON
{
    "require": {
        "mongator/behaviors": "1.0.*"
    }
}
```


Examples
--------
On your document definition just add a new array named behaviors, just like this:

```php
'Model\MyCollecion' => array(
    'fields' => array(
        'title' => 'string',
    ),
    'behaviors' => array(
        array('class' => 'Mongator\Behavior\Tokenizable'),
        array('class' => 'Mongator\Behavior\Archivable'),
    ),
),
```

Tests
-----

Tests are in the `tests` folder.
To run them, you need PHPUnit.
Example:

    $ phpunit --configuration phpunit.xml.dist


License
-------

MIT, see [LICENSE](LICENSE)