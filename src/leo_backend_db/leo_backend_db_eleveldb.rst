leo\_backend\_db\_eleveldb
=================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

Handling database operation for eleveldb.

**References**

-  https://github.com/leo-project/leo\_backend\_db/blob/master/src/leo\_backend\_db\_eleveldb.erl

Description
-----------

Handling database operation for eleveldb

Function Index
--------------

+-------------------------------------------+--------------------------------------------------------------------+
| `close/1 <#close-1>`__                    | Close a leveldb data store and flush any pending writes to disk.   |
+-------------------------------------------+--------------------------------------------------------------------+
| `delete/2 <#delete-2>`__                  | Delete an object from the eleveldb.                                |
+-------------------------------------------+--------------------------------------------------------------------+
| `first/1 <#first-1>`__                    | Retrieve a first record from eleveldb.                             |
+-------------------------------------------+--------------------------------------------------------------------+
| `get/2 <#get-2>`__                        | Retrieve an object from the eleveldb.                              |
+-------------------------------------------+--------------------------------------------------------------------+
| `open/1 <#open-1>`__                      | Open a new or existing leveldb datastore for read-only access.     |
+-------------------------------------------+--------------------------------------------------------------------+
| `open/2 <#open-2>`__                      |                                                                    |
+-------------------------------------------+--------------------------------------------------------------------+
| `prefix\_search/4 <#prefix_search-4>`__   | Retrieve objects from eleveldb by a keyword.                       |
+-------------------------------------------+--------------------------------------------------------------------+
| `put/3 <#put-3>`__                        | Insert an object into the eleveldb.                                |
+-------------------------------------------+--------------------------------------------------------------------+
| `status/1 <#status-1>`__                  | Get the status information for this eleveldb backend.              |
+-------------------------------------------+--------------------------------------------------------------------+

Function Details
----------------

close/1
~~~~~~~

``close(Handler) -> ok``

-  ``Handler = binary()``

Close a leveldb data store and flush any pending writes to disk

delete/2
~~~~~~~~

``delete(Handler, Key) -> ok | {error, any()}``

-  ``Handler = binary()``
-  ``Key = binary()``

Delete an object from the eleveldb.

first/1
~~~~~~~

``first(Handler) -> {ok, any()} | not_found | {error, any()}``

-  ``Handler = binary()``

Retrieve a first record from eleveldb.

get/2
~~~~~

``get(Handler, Key) -> {ok, binary()} | not_found | {error, any()}``

-  ``Handler = binary()``
-  ``Key = binary()``

Retrieve an object from the eleveldb.

open/1
~~~~~~

``open(Path) -> {error, any()} | {ok, pid()}``

-  ``Path = string()``

Open a new or existing leveldb datastore for read-only access

open/2
~~~~~~

``open(Path, Config) -> {error, any()} | {ok, pid()}``

-  ``Path = string()``
-  ``Config = [tuple()]``

prefix\_search/4
~~~~~~~~~~~~~~~~

``prefix_search(Handler, Key, Fun, MaxKeys) -> {ok, [term()]} | not_found | {error, any()}``

-  ``Handler = binary()``
-  ``Key = binary()``
-  ``Fun = function()``
-  ``MaxKeys = integer()``

Retrieve objects from eleveldb by a keyword.

put/3
~~~~~

``put(Handler, Key, Value) -> ok | {error, any()}``

-  ``Handler = binary()``
-  ``Key = binary()``
-  ``Value = binary()``

Insert an object into the eleveldb.

status/1
~~~~~~~~

``status(Handler) -> [{atom(), term()}]``

-  ``Handler = binary()``

Get the status information for this eleveldb backend
