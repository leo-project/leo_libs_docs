leo\_object\_storage\_api
================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The object staorge's API.

**References**

-  https://github.com/leo-project/leo\_object\_storage/blob/master/src/leo\_object\_storage\_api.erl

Description
-----------

The object staorge's API

Function Index
--------------

+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `add\_incorrect\_data/1 <#add_incorrect_data-1>`__                         | Add incorrect datas on debug purpose.                                                         |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `compact\_data/0 <#compact_data-0>`__                                      | Execute data-compaction.                                                                      |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `compact\_data/1 <#compact_data-1>`__                                      |                                                                                               |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `compact\_data/2 <#compact_data-2>`__                                      |                                                                                               |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `compact\_data/3 <#compact_data-3>`__                                      |                                                                                               |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `delete/2 <#delete-2>`__                                                   | Remove an object from the object-storage.                                                     |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `diagnose\_data/0 <#diagnose_data-0>`__                                    | Diagnode the data.                                                                            |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `diagnose\_data/1 <#diagnose_data-1>`__                                    |                                                                                               |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `fetch\_by\_addr\_id/2 <#fetch_by_addr_id-2>`__                            | Fetch objects by ring-address-id.                                                             |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `fetch\_by\_addr\_id/3 <#fetch_by_addr_id-3>`__                            |                                                                                               |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `fetch\_by\_key/2 <#fetch_by_key-2>`__                                     | Fetch objects by key (object-name).                                                           |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `fetch\_by\_key/3 <#fetch_by_key-3>`__                                     |                                                                                               |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get/1 <#get-1>`__                                                         | Retrieve an object and a metadata from the object-storage.                                    |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get/3 <#get-3>`__                                                         |                                                                                               |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get\_object\_storage\_pid/1 <#get_object_storage_pid-1>`__                | Retrieve the storage process-id.                                                              |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get\_object\_storage\_pid\_first/0 <#get_object_storage_pid_first-0>`__   | Retrieve the first record of object-storage pids.                                             |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `head/1 <#head-1>`__                                                       | Retrieve a metadata from the object-storage.                                                  |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `head\_with\_calc\_md5/2 <#head_with_calc_md5-2>`__                        | Retrieve a metada/data from backend\_db/object-storage AND calc MD5 based on the body data.   |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `put/2 <#put-2>`__                                                         | Insert an object into the object-storage.                                                     |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `start/1 <#start-1>`__                                                     | Create object-storage processes.                                                              |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `start\_with\_path/1 <#start_with_path-1>`__                               |                                                                                               |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `stats/0 <#stats-0>`__                                                     | Retrieve the storage stats.                                                                   |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `store/2 <#store-2>`__                                                     | Store metadata and data.                                                                      |
+----------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+

Function Details
----------------

add\_incorrect\_data/1
~~~~~~~~~~~~~~~~~~~~~~

| ``add_incorrect_data(Bin::binary()) -> ok | {error, any()}``

Add incorrect datas on debug purpose

compact\_data/0
~~~~~~~~~~~~~~~

| ``compact_data() -> term()``

Execute data-compaction

compact\_data/1
~~~~~~~~~~~~~~~

``compact_data(MaxConn) -> term()``

-  ``MaxConn = integer()``

compact\_data/2
~~~~~~~~~~~~~~~

``compact_data(MaxConn, CallbackFun) -> term()``

-  ``MaxConn = integer()``
-  ``CallbackFun = function()``

compact\_data/3
~~~~~~~~~~~~~~~

``compact_data(TargetPids, MaxConn, CallbackFun) -> term()``

-  ``TargetPids = [atom()]``
-  ``MaxConn = integer()``
-  ``CallbackFun = function()``

delete/2
~~~~~~~~

``delete(AddrIdAndKey, Object) -> ok | {error, any()}``

-  ``AddrIdAndKey = addrid_and_key()``
-  ``Object = #'?OBJECT'{}``

Remove an object from the object-storage

diagnose\_data/0
~~~~~~~~~~~~~~~~

| ``diagnose_data() -> term()``

Diagnode the data

diagnose\_data/1
~~~~~~~~~~~~~~~~

``diagnose_data(Path) -> ok | {error, any()}``

-  ``Path = string()``

fetch\_by\_addr\_id/2
~~~~~~~~~~~~~~~~~~~~~

``fetch_by_addr_id(AddrId, Fun) -> {ok, []} | not_found``

-  ``AddrId = non_neg_integer()``
-  ``Fun = function() | undefined``

Fetch objects by ring-address-id

fetch\_by\_addr\_id/3
~~~~~~~~~~~~~~~~~~~~~

``fetch_by_addr_id(AddrId, Fun, MaxKeys) -> {ok, []} | not_found``

-  ``AddrId = non_neg_integer()``
-  ``Fun = function() | undefined``
-  ``MaxKeys = non_neg_integer() | undefined``

fetch\_by\_key/2
~~~~~~~~~~~~~~~~

``fetch_by_key(Key, Fun) -> {ok, list()} | not_found``

-  ``Key = binary()``
-  ``Fun = function()``

Fetch objects by key (object-name)

fetch\_by\_key/3
~~~~~~~~~~~~~~~~

``fetch_by_key(Key, Fun, MaxKeys) -> {ok, list()} | not_found``

-  ``Key = binary()``
-  ``Fun = function()``
-  ``MaxKeys = non_neg_integer() | undefined``

get/1
~~~~~

``get(AddrIdAndKey) -> {ok, list()} | not_found | {error, any()}``

-  ``AddrIdAndKey = addrid_and_key()``

Retrieve an object and a metadata from the object-storage

get/3
~~~~~

``get(AddrIdAndKey, StartPos, EndPos) -> {ok, #'?METADATA'{}, #'?OBJECT'{}} | not_found | {error, any()}``

-  ``AddrIdAndKey = addrid_and_key()``
-  ``StartPos = non_neg_integer()``
-  ``EndPos = non_neg_integer()``

get\_object\_storage\_pid/1
~~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_object_storage_pid(Arg) -> [atom()]``

-  ``Arg = all | any()``

Retrieve the storage process-id

get\_object\_storage\_pid\_first/0
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_object_storage_pid_first() -> Id``

-  ``Id = atom()``

Retrieve the first record of object-storage pids

head/1
~~~~~~

``head(AddrIdAndKey) -> {ok, binary()} | not_found | {error, any()}``

-  ``AddrIdAndKey = addrid_and_key()``

Retrieve a metadata from the object-storage

head\_with\_calc\_md5/2
~~~~~~~~~~~~~~~~~~~~~~~

``head_with_calc_md5(AddrIdAndKey, MD5Context) -> {ok, metadata, any()} | {error, any()}``

-  ``AddrIdAndKey = addrid_and_key()``
-  ``MD5Context = any()``

Retrieve a metada/data from backend\_db/object-storage AND calc MD5
based on the body data

put/2
~~~~~

``put(AddrIdAndKey, Object) -> {ok, integer()} | {error, any()}``

-  ``AddrIdAndKey = addrid_and_key()``
-  ``Object = #'?OBJECT'{}``

Insert an object into the object-storage

start/1
~~~~~~~

``start(Option) -> ok | {error, any()}``

-  ``Option = [{pos_integer(), string()}]``

Create object-storage processes

start\_with\_path/1
~~~~~~~~~~~~~~~~~~~

``start_with_path(Path) -> ok | {error, any()}``

-  ``Path = string()``

stats/0
~~~~~~~

| ``stats() -> {ok, list()} | not_found``

Retrieve the storage stats

store/2
~~~~~~~

``store(Metadata, Bin) -> ok | {error, any()}``

-  ``Metadata = #'?METADATA'{}``
-  ``Bin = binary()``

Store metadata and data
