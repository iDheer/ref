TinyDB
======

TinyDB is a lightweight, document-oriented database written in pure Python
with no external dependencies.

Usage
-----

.. code-block:: python

    >>> from tinydb import TinyDB, Query
    >>> db = TinyDB('db.json')
    >>> db.insert({'name': 'John', 'age': 22})
    >>> User = Query()
    >>> db.search(User.name == 'John')
    [{'name': 'John', 'age': 22}]
    >>> db.search(User.age.between(18, 30))
    [{'name': 'John', 'age': 22}]

Gzip-compressed storage:

.. code-block:: python

    >>> from tinydb.storages import CompressedJSONStorage
    >>> db = TinyDB('db.json.gz', storage=CompressedJSONStorage)

License: MIT (see ``LICENSE``).
