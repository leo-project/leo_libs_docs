leo\_backend\_db\_api
============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_backend\_db's API.

**References**

-  ```https://github.com/leo-project/leo_backend_db/blob/master/src/leo_backend_db_api.erl`` <https://github.com/leo-project/leo_backend_db/blob/master/src/leo_backend_db_api.erl>`__

Description
-----------

leo\_backend\_db's API

Function Index
--------------

+----------------------------------------------------------+--------------------------------------------------------+
| `delete/2 <#delete-2>`__                                 | Delete an object from backend-db.                      |
+----------------------------------------------------------+--------------------------------------------------------+
| `fetch/3 <#fetch-3>`__                                   | Fetch objects from backend-db by key with function.    |
+----------------------------------------------------------+--------------------------------------------------------+
| `fetch/4 <#fetch-4>`__                                   |                                                        |
+----------------------------------------------------------+--------------------------------------------------------+
| `finish\_compaction/2 <#finish_compaction-2>`__          | End the data-compaction.                               |
+----------------------------------------------------------+--------------------------------------------------------+
| `first/1 <#first-1>`__                                   | Retrieve a first record from backend-db.               |
+----------------------------------------------------------+--------------------------------------------------------+
| `get/2 <#get-2>`__                                       | Retrieve an object from backend-db.                    |
+----------------------------------------------------------+--------------------------------------------------------+
| `get\_db\_raw\_filepath/1 <#get_db_raw_filepath-1>`__    | get the database filepath for calculating disk size.   |
+----------------------------------------------------------+--------------------------------------------------------+
| `new/4 <#new-4>`__                                       | create storage-processes.                              |
+----------------------------------------------------------+--------------------------------------------------------+
| `put/3 <#put-3>`__                                       | Insert an object into backend-db.                      |
+----------------------------------------------------------+--------------------------------------------------------+
| `put\_value\_to\_new\_db/3 <#put_value_to_new_db-3>`__   | Put a record to a new db.                              |
+----------------------------------------------------------+--------------------------------------------------------+
| `run\_compaction/1 <#run_compaction-1>`__                | Start the data-compaction.                             |
+----------------------------------------------------------+--------------------------------------------------------+
| `status/1 <#status-1>`__                                 | Retrieve status from backend-db.                       |
+----------------------------------------------------------+--------------------------------------------------------+
| `stop/1 <#stop-1>`__                                     | Stop the instance.                                     |
+----------------------------------------------------------+--------------------------------------------------------+

Function Details
----------------

delete/2
~~~~~~~~

``delete(InstanceName, KeyBin) -> ok | {error, any()}``

-  ``InstanceName = atom()``
-  ``KeyBin = binary()``

Delete an object from backend-db.

fetch/3
~~~~~~~

``fetch(InstanceName, KeyBin, Fun) -> {ok, list()} | not_found | {error, any()}``

-  ``InstanceName = atom()``
-  ``KeyBin = binary()``
-  ``Fun = function()``

Fetch objects from backend-db by key with function.

fetch/4
~~~~~~~

``fetch(InstanceName, KeyBin, Fun, MaxKeys) -> {ok, list()} | not_found | {error, any()}``

-  ``InstanceName = atom()``
-  ``KeyBin = binary()``
-  ``Fun = function()``
-  ``MaxKeys = pos_integer()``

finish\_compaction/2
~~~~~~~~~~~~~~~~~~~~

``finish_compaction(InstanceName, Commit) -> ok | {error, any()}``

-  ``InstanceName = atom()``
-  ``Commit = boolean()``

End the data-compaction

first/1
~~~~~~~

``first(InstanceName) -> {ok, list()} | {error, any()}``

-  ``InstanceName = atom()``

Retrieve a first record from backend-db.

get/2
~~~~~

``get(InstanceName, KeyBin) -> {ok, binary()} | not_found | {error, any()}``

-  ``InstanceName = atom()``
-  ``KeyBin = binary()``

Retrieve an object from backend-db.

get\_db\_raw\_filepath/1
~~~~~~~~~~~~~~~~~~~~~~~~

``get_db_raw_filepath(InstanceName) -> {ok, string()} | {error, any()}``

-  ``InstanceName = atom()``

get the database filepath for calculating disk size

new/4
~~~~~

``new(InstanceName, NumOfDBProcs, BackendDB, DBRootPath) -> ok | {error, any()}``

-  ``InstanceName = atom()``
-  ``NumOfDBProcs = pos_integer()``
-  ``BackendDB = backend_db()``
-  ``DBRootPath = string()``

create storage-processes.

put/3
~~~~~

``put(InstanceName, KeyBin, ValueBin) -> ok | {error, any()}``

-  ``InstanceName = atom()``
-  ``KeyBin = binary()``
-  ``ValueBin = binary()``

Insert an object into backend-db.

put\_value\_to\_new\_db/3
~~~~~~~~~~~~~~~~~~~~~~~~~

``put_value_to_new_db(InstanceName, KeyBin, ValueBin) -> ok | {error, any()}``

-  ``InstanceName = atom()``
-  ``KeyBin = binary()``
-  ``ValueBin = binary()``

Put a record to a new db

run\_compaction/1
~~~~~~~~~~~~~~~~~

``run_compaction(InstanceName) -> ok | {error, any()}``

-  ``InstanceName = atom()``

Start the data-compaction

status/1
~~~~~~~~

``status(InstanceName) -> [{atom(), term()}]``

-  ``InstanceName = atom()``

Retrieve status from backend-db.

stop/1
~~~~~~

``stop(InstanceName) -> ok | {error, any()}``

-  ``InstanceName = atom()``

Stop the instance
