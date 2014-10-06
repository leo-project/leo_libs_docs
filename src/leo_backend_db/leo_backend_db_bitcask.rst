leo\_backend\_db\_bitcask
================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

Handling database operation for bitcask.

**References**

-  https://github.com/leo-project/leo\_backend\_db/blob/master/src/leo\_backend\_db\_bitcask.erl

Description
-----------

Handling database operation for bitcask

Function Index
--------------

+-------------------------------------------+---------------------------------------------------------------------+
| `close/1 <#close-1>`__                    | Close a bitcask data store and flush any pending writes to disk.    |
+-------------------------------------------+---------------------------------------------------------------------+
| `delete/2 <#delete-2>`__                  | Delete an object from bitcask.                                      |
+-------------------------------------------+---------------------------------------------------------------------+
| `first/1 <#first-1>`__                    | Retrieve a first record from bitcask.                               |
+-------------------------------------------+---------------------------------------------------------------------+
| `get/2 <#get-2>`__                        | Retrieve an object from bitcask.                                    |
+-------------------------------------------+---------------------------------------------------------------------+
| `open/1 <#open-1>`__                      | Open a new or existing bitcask datastore for read-only access.      |
+-------------------------------------------+---------------------------------------------------------------------+
| `open/2 <#open-2>`__                      |                                                                     |
+-------------------------------------------+---------------------------------------------------------------------+
| `prefix\_search/4 <#prefix_search-4>`__   | Retrieve an objects from bitcask by the keyword and the function.   |
+-------------------------------------------+---------------------------------------------------------------------+
| `put/3 <#put-3>`__                        | Insert an object into bitcask.                                      |
+-------------------------------------------+---------------------------------------------------------------------+
| `status/1 <#status-1>`__                  | Retrive the status information for this bitcask backend.            |
+-------------------------------------------+---------------------------------------------------------------------+

Function Details
----------------

close/1
~~~~~~~

``close(Handler) -> ok``

-  ``Handler = reference()``

Close a bitcask data store and flush any pending writes to disk

delete/2
~~~~~~~~

``delete(Handler, Key) -> ok | {error, any()}``

-  ``Handler = reference()``
-  ``Key = binary()``

Delete an object from bitcask.

first/1
~~~~~~~

``first(Handler) -> {ok, any()} | not_found | {error, any()}``

-  ``Handler = reference()``

Retrieve a first record from bitcask

get/2
~~~~~

``get(Handler, Key) -> not_found | {ok, binary()} | {error, any()}``

-  ``Handler = reference()``
-  ``Key = binary()``

Retrieve an object from bitcask.

open/1
~~~~~~

``open(Path) -> {ok, pid()} | {error, any()}``

-  ``Path = string()``

Open a new or existing bitcask datastore for read-only access

open/2
~~~~~~

``open(Path, Options) -> {ok, pid()} | {error, any()}``

-  ``Path = string()``
-  ``Options = list()``

prefix\_search/4
~~~~~~~~~~~~~~~~

``prefix_search(Handler, Key, Fun, MaxKeys) -> {ok, [any()]} | not_found | {error, any()}``

-  ``Handler = reference()``
-  ``Key = binary()``
-  ``Fun = function()``
-  ``MaxKeys = pos_integer()``

Retrieve an objects from bitcask by the keyword and the function

put/3
~~~~~

``put(Handler, Key, Value) -> ok | {error, any()}``

-  ``Handler = reference()``
-  ``Key = binary()``
-  ``Value = binary()``

Insert an object into bitcask.

status/1
~~~~~~~~

``status(Handler) -> [{atom(), term()}]``

-  ``Handler = reference()``

Retrive the status information for this bitcask backend
