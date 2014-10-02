leo\_object\_storage\_server
===================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The object storage server.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  https://github.com/leo-project/leo\_object\_storage/blob/master/src/leo\_object\_storage\_server.erl

Description
-----------

The object storage server

Function Index
--------------

+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `add\_incorrect\_data/2 <#add_incorrect_data-2>`__                 | Store metadata and data.                                                                      |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `append\_compaction\_history/2 <#append_compaction_history-2>`__   | Append the history in the state.                                                              |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `close/1 <#close-1>`__                                             | Close the object-container.                                                                   |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__                                | Convert process state when code is changed.                                                   |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `delete/2 <#delete-2>`__                                           | Remove an object from the object-storage - (logical-delete).                                  |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `fetch/4 <#fetch-4>`__                                             | Retrieve objects from the object-storage by Key and Function.                                 |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get/4 <#get-4>`__                                                 | Retrieve an object from the object-storage.                                                   |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get\_avs\_version\_bin/1 <#get_avs_version_bin-1>`__              | Get AVS format version binary like "LeoFS AVS-2.2".                                           |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get\_backend\_info/2 <#get_backend_info-2>`__                     | Retrieve object-storage/metadata-storage info.                                                |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get\_compaction\_worker/1 <#get_compaction_worker-1>`__           | Retrieve the compaction worker.                                                               |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get\_stats/1 <#get_stats-1>`__                                    | Retrieve the storage stats specfied by Id which contains number of objects and so on.         |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__                                | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.                   |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__                                | Handling cast message.                                                                        |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__                                | Handling all non call/cast messages.                                                          |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `head/2 <#head-2>`__                                               | Retrieve an object's metadata from the object-storage.                                        |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `head\_with\_calc\_md5/3 <#head_with_calc_md5-3>`__                | Retrieve a metada/data from backend\_db/object-storage AND calc MD5 based on the body data.   |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                                               | Initiates the server.                                                                         |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `lock/1 <#lock-1>`__                                               | Retrieve object-storage/metadata-storage info.                                                |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `put/2 <#put-2>`__                                                 | Insert an object and an object's metadata into the object-storage.                            |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `set\_stats/2 <#set_stats-2>`__                                    | Retrieve the storage stats specfied by Id which contains number of objects and so on.         |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `start\_link/6 <#start_link-6>`__                                  | Starts the server.                                                                            |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `start\_link/7 <#start_link-7>`__                                  | Starts the server with strict-check.                                                          |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                                               | Stop this server.                                                                             |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `store/3 <#store-3>`__                                             | Store metadata and data.                                                                      |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `switch\_container/4 <#switch_container-4>`__                      | Open the object-container.                                                                    |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__                                     | This function is called by a gen\_server when it is about to terminate.                       |
+--------------------------------------------------------------------+-----------------------------------------------------------------------------------------------+

Function Details
----------------

add\_incorrect\_data/2
~~~~~~~~~~~~~~~~~~~~~~

| ``add_incorrect_data(Id::atom(), Bin::binary()) -> ok | {error, any()}``

Store metadata and data

append\_compaction\_history/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``append_compaction_history(Id, History) -> ok``

-  ``Id = atom()``
-  ``History = tuple()``

Append the history in the state

close/1
~~~~~~~

``close(Id) -> ok``

-  ``Id = atom()``

Close the object-container

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

delete/2
~~~~~~~~

``delete(Id, Object) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Object = #'?OBJECT'{}``

Remove an object from the object-storage - (logical-delete)

fetch/4
~~~~~~~

``fetch(Id, Key, Fun, MaxKeys) -> {ok, list()} | {error, any()}``

-  ``Id = atom()``
-  ``Key = any()``
-  ``Fun = function()``
-  ``MaxKeys = non_neg_integer() | undefined``

Retrieve objects from the object-storage by Key and Function

get/4
~~~~~

``get(Id, AddrIdAndKey, StartPos, EndPos) -> {ok, #'?METADATA'{}, #'?OBJECT'{}} | not_found | {error, any()}``

-  ``Id = atom()``
-  ``AddrIdAndKey = addrid_and_key()``
-  ``StartPos = non_neg_integer()``
-  ``EndPos = non_neg_integer()``

Retrieve an object from the object-storage

get\_avs\_version\_bin/1
~~~~~~~~~~~~~~~~~~~~~~~~

``get_avs_version_bin(Id) -> ok``

-  ``Id = atom()``

Get AVS format version binary like "LeoFS AVS-2.2"

get\_backend\_info/2
~~~~~~~~~~~~~~~~~~~~

``get_backend_info(Id, ServerType) -> {ok, #backend_info{}}``

-  ``Id = atom()``
-  ``ServerType = '?SERVER_OBJ_STORAGE'``

Retrieve object-storage/metadata-storage info

get\_compaction\_worker/1
~~~~~~~~~~~~~~~~~~~~~~~~~

``get_compaction_worker(Id) -> {ok, CompactionWorkerId}``

-  ``Id = atom()``
-  ``CompactionWorkerId = atom()``

Retrieve the compaction worker

get\_stats/1
~~~~~~~~~~~~

``get_stats(Id) -> {ok, #storage_stats{}} | {error, any()}``

-  ``Id = atom()``

Retrieve the storage stats specfied by Id which contains number of
objects and so on.

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(X1, From, State) -> any()``

gen\_server callback - Module:handle\_call(Request, From, State) ->
Result

handle\_cast/2
~~~~~~~~~~~~~~

``handle_cast(Msg, State) -> any()``

Handling cast message

gen\_server callback - Module:handle\_cast(Request, State) -> Result.

handle\_info/2
~~~~~~~~~~~~~~

``handle_info(Info, State) -> any()``

Handling all non call/cast messages

gen\_server callback - Module:handle\_info(Info, State) -> Result.

head/2
~~~~~~

``head(Id, AddrIdAndKey) -> {ok, binary()} | not_found | {error, any()}``

-  ``Id = atom()``
-  ``AddrIdAndKey = addrid_and_key()``

Retrieve an object's metadata from the object-storage

head\_with\_calc\_md5/3
~~~~~~~~~~~~~~~~~~~~~~~

``head_with_calc_md5(Id, Key, MD5Context) -> {ok, #'?METADATA'{}, any()} | {error, any()}``

-  ``Id = atom()``
-  ``Key = tuple()``
-  ``MD5Context = any()``

Retrieve a metada/data from backend\_db/object-storage AND calc MD5
based on the body data

init/1
~~~~~~

``init(X1) -> any()``

Initiates the server

lock/1
~~~~~~

``lock(Id) -> ok``

-  ``Id = atom()``

Retrieve object-storage/metadata-storage info

put/2
~~~~~

``put(Id, Object) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Object = #'?OBJECT'{}``

Insert an object and an object's metadata into the object-storage

set\_stats/2
~~~~~~~~~~~~

``set_stats(Id, StorageStats) -> ok``

-  ``Id = atom()``
-  ``StorageStats = #storage_stats{}``

Retrieve the storage stats specfied by Id which contains number of
objects and so on.

start\_link/6
~~~~~~~~~~~~~

``start_link(Id, SeqNo, MetaDBId, CompactionWorkerId, DiagnosisLogId, RootPath) -> {ok, pid()} | {error, any()}``

-  ``Id = atom()``
-  ``SeqNo = non_neg_integer()``
-  ``MetaDBId = atom()``
-  ``CompactionWorkerId = atom()``
-  ``DiagnosisLogId = atom()``
-  ``RootPath = string()``

Starts the server

start\_link/7
~~~~~~~~~~~~~

``start_link(Id, SeqNo, MetaDBId, CompactionWorkerId, DiagnosisLogId, RootPath, IsStrictCheck) -> {ok, pid()} | {error, any()}``

-  ``Id = atom()``
-  ``SeqNo = non_neg_integer()``
-  ``MetaDBId = atom()``
-  ``CompactionWorkerId = atom()``
-  ``DiagnosisLogId = atom()``
-  ``RootPath = string()``
-  ``IsStrictCheck = boolean()``

Starts the server with strict-check

stop/1
~~~~~~

``stop(Id) -> ok``

-  ``Id = atom()``

Stop this server

store/3
~~~~~~~

``store(Id, Metadata, Bin) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Metadata = #'?METADATA'{}``
-  ``Bin = binary()``

Store metadata and data

switch\_container/4
~~~~~~~~~~~~~~~~~~~

``switch_container(Id, FilePath, NumOfActiveObjs, SizeOfActiveObjs) -> ok``

-  ``Id = atom()``
-  ``FilePath = string()``
-  ``NumOfActiveObjs = non_neg_integer()``
-  ``SizeOfActiveObjs = non_neg_integer()``

Open the object-container

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason.
