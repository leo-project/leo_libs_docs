leo\_s3\_libs
====================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The s3-libs API.

**References**

-  https://github.com/leo-project/leo\_s3\_libs/blob/master/src/leo\_s3\_libs.erl

Description
-----------

The s3-libs API

Function Index
--------------

+-------------------------------------------------+----------------------------------+
| `get\_checksums/0 <#get_checksums-0>`__         | update\_providers(slave only).   |
+-------------------------------------------------+----------------------------------+
| `start/1 <#start-1>`__                          | Launch or create Mnesia/ETS.     |
+-------------------------------------------------+----------------------------------+
| `start/2 <#start-2>`__                          |                                  |
+-------------------------------------------------+----------------------------------+
| `update\_providers/1 <#update_providers-1>`__   | update\_providers(slave only).   |
+-------------------------------------------------+----------------------------------+

Function Details
----------------

get\_checksums/0
~~~~~~~~~~~~~~~~

| ``get_checksums() -> {ok, #s3_tbls_checksum{}}``

update\_providers(slave only)

start/1
~~~~~~~

``start(Role) -> ok``

-  ``Role = master | slave``

Launch or create Mnesia/ETS

start/2
~~~~~~~

``start(Role, Options) -> ok``

-  ``Role = master | slave``
-  ``Options = list()``

update\_providers/1
~~~~~~~~~~~~~~~~~~~

``update_providers(Provider) -> ok``

-  ``Provider = list()``

update\_providers(slave only)
