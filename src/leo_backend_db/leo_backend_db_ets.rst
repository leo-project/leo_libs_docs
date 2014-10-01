leo\_backend\_db\_ets
============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

Handling database operation for ETS.

**References**

-  ```https://github.com/leo-project/leo_backend_db/blob/master/src/leo_backend_db_ets.erl`` <https://github.com/leo-project/leo_backend_db/blob/master/src/leo_backend_db_ets.erl>`__

Description
-----------

Handling database operation for ETS

Function Index
--------------

+-------------------------------------------+--------------------------------------------+
| `close/1 <#close-1>`__                    | Close a ets data store.                    |
+-------------------------------------------+--------------------------------------------+
| `delete/2 <#delete-2>`__                  | Delete an object from the ets.             |
+-------------------------------------------+--------------------------------------------+
| `first/1 <#first-1>`__                    | Retrieve a first record from the ets.      |
+-------------------------------------------+--------------------------------------------+
| `get/2 <#get-2>`__                        | Retrieve an object from the ets.           |
+-------------------------------------------+--------------------------------------------+
| `open/1 <#open-1>`__                      | Open a new ets datastore.                  |
+-------------------------------------------+--------------------------------------------+
| `open/2 <#open-2>`__                      |                                            |
+-------------------------------------------+--------------------------------------------+
| `prefix\_search/4 <#prefix_search-4>`__   | Retrieve objects from ets by a keyword.    |
+-------------------------------------------+--------------------------------------------+
| `put/3 <#put-3>`__                        | Insert an object into ets.                 |
+-------------------------------------------+--------------------------------------------+
| `status/1 <#status-1>`__                  | Get the status information for this ets.   |
+-------------------------------------------+--------------------------------------------+

Function Details
----------------

close/1
~~~~~~~

``close(Table) -> ok``

-  ``Table = atom()``

Close a ets data store

delete/2
~~~~~~~~

``delete(Table, Key) -> ok | not_found | {error, any()}``

-  ``Table = atom()``
-  ``Key = binary()``

Delete an object from the ets

first/1
~~~~~~~

``first(Table) -> {ok, any()} | not_found | {error, any()}``

-  ``Table = pid()``

Retrieve a first record from the ets

get/2
~~~~~

``get(Table, Key) -> not_found | {ok, binary()} | {error, any()}``

-  ``Table = atom()``
-  ``Key = binary()``

Retrieve an object from the ets.

open/1
~~~~~~

``open(Table) -> ok``

-  ``Table = atom() | string()``

Open a new ets datastore

open/2
~~~~~~

``open(Table, Option) -> ok``

-  ``Table = atom() | string()``
-  ``Option = [atom()]``

prefix\_search/4
~~~~~~~~~~~~~~~~

``prefix_search(Table, Key, Fun, MaxKeys) -> {ok, list()} | not_found | {error, any()}``

-  ``Table = pid()``
-  ``Key = binary()``
-  ``Fun = function()``
-  ``MaxKeys = pos_integer()``

Retrieve objects from ets by a keyword.

put/3
~~~~~

``put(Table, Key, Value) -> ok | {error, any()}``

-  ``Table = pid()``
-  ``Key = binary()``
-  ``Value = binary()``

Insert an object into ets.

status/1
~~~~~~~~

``status(Table) -> [any()] | undefined``

-  ``Table = atom()``

Get the status information for this ets.
