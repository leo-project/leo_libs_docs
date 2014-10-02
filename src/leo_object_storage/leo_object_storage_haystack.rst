leo\_object\_storage\_haystack
=====================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The object storage implementation - haystack.

**References**

-  https://github.com/leo-project/leo\_object\_storage/blob/master/src/leo\_object\_storage\_haystack.erl

Description
-----------

The object storage implementation - haystack

Function Index
--------------

+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `calc\_obj\_size/1 <#calc_obj_size-1>`__                     | Open and clreate a file.                                                                      |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `calc\_obj\_size/2 <#calc_obj_size-2>`__                     |                                                                                               |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `close/2 <#close-2>`__                                       | Close file handlers.                                                                          |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `delete/3 <#delete-3>`__                                     | Remove an object and a metadata from the object-storage.                                      |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `fetch/4 <#fetch-4>`__                                       | Fetch objects from the object-storage.                                                        |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get/3 <#get-3>`__                                           | Retrieve an object and a metadata.                                                            |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get/6 <#get-6>`__                                           | Retrieve part of an object and a metadata.                                                    |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get\_obj\_for\_new\_cntnr/1 <#get_obj_for_new_cntnr-1>`__   | Retrieve a file from object-container when compacting.                                        |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `get\_obj\_for\_new\_cntnr/2 <#get_obj_for_new_cntnr-2>`__   |                                                                                               |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `head/2 <#head-2>`__                                         | Retrieve a metada from backend\_db from the object-storage.                                   |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `head\_with\_calc\_md5/4 <#head_with_calc_md5-4>`__          | Retrieve a metada/data from backend\_db/object-storage AND calc MD5 based on the body data.   |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `open/1 <#open-1>`__                                         | Open a new or existing datastore.                                                             |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `open/2 <#open-2>`__                                         |                                                                                               |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `put/3 <#put-3>`__                                           | Insert an object and a metadata into the object-storage.                                      |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `put\_obj\_to\_new\_cntnr/4 <#put_obj_to_new_cntnr-4>`__     | Insert an object into the object-container when compacting.                                   |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+
| `store/4 <#store-4>`__                                       | Store metadata and binary.                                                                    |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------+

Function Details
----------------

calc\_obj\_size/1
~~~~~~~~~~~~~~~~~

``calc_obj_size(MetadataOrObject) -> non_neg_integer()``

-  ``MetadataOrObject = #'?METADATA'{} | #'?OBJECT'{}``

Open and clreate a file.

calc\_obj\_size/2
~~~~~~~~~~~~~~~~~

``calc_obj_size(KSize, DSize) -> non_neg_integer()``

-  ``KSize = non_neg_integer()``
-  ``DSize = non_neg_integer()``

close/2
~~~~~~~

``close(WriteHandler, ReadHandler) -> ok``

-  ``WriteHandler = port() | any()``
-  ``ReadHandler = port() | any()``

Close file handlers.

delete/3
~~~~~~~~

``delete(MetaDBId, StorageInfo, Object) -> ok | {error, any()}``

-  ``MetaDBId = atom()``
-  ``StorageInfo = #backend_info{}``
-  ``Object = #'?OBJECT'{}``

Remove an object and a metadata from the object-storage

fetch/4
~~~~~~~

``fetch(MetaDBId, Key, Fun, MaxKeys) -> {ok, list()} | not_found | {error, any()}``

-  ``MetaDBId = atom()``
-  ``Key = binary()``
-  ``Fun = function()``
-  ``MaxKeys = pos_integer() | undefined``

Fetch objects from the object-storage

get/3
~~~~~

``get(MetaDBId, StorageInfo, Key) -> {ok, #'?METADATA'{}, #'?OBJECT'{}} | {error, any()}``

-  ``MetaDBId = atom()``
-  ``StorageInfo = #backend_info{}``
-  ``Key = binary()``

Retrieve an object and a metadata

get/6
~~~~~

``get(MetaDBId, StorageInfo, Key, StartPos, EndPos, IsStrictCheck) -> {ok, #'?METADATA'{}, #'?OBJECT'{}} | {error, any()}``

-  ``MetaDBId = atom()``
-  ``StorageInfo = #backend_info{}``
-  ``Key = binary()``
-  ``StartPos = non_neg_integer()``
-  ``EndPos = non_neg_integer()``
-  ``IsStrictCheck = boolean()``

Retrieve part of an object and a metadata

get\_obj\_for\_new\_cntnr/1
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| ``get_obj_for_new_cntnr(ReadHandler::pid()) -> ok | {error, any()}``

Retrieve a file from object-container when compacting.

get\_obj\_for\_new\_cntnr/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| ``get_obj_for_new_cntnr(ReadHandler::pid(), Offset::integer()) -> ok | {error, any()}``

head/2
~~~~~~

``head(MetaDBId, Key) -> {ok, binary()} | not_found | {error, any()}``

-  ``MetaDBId = atom()``
-  ``Key = binary()``

Retrieve a metada from backend\_db from the object-storage

head\_with\_calc\_md5/4
~~~~~~~~~~~~~~~~~~~~~~~

``head_with_calc_md5(MetaDBId, StorageInfo, Key, MD5Context) -> {ok, #'?METADATA'{}} | not_found | {error, any()}``

-  ``MetaDBId = atom()``
-  ``StorageInfo = #backend_info{}``
-  ``Key = binary()``
-  ``MD5Context = any()``

Retrieve a metada/data from backend\_db/object-storage AND calc MD5
based on the body data

open/1
~~~~~~

``open(FilePath) -> {ok, port(), port(), binary()} | {error, any()}``

-  ``FilePath = string()``

Open a new or existing datastore

open/2
~~~~~~

``open(FilePath, Option) -> {ok, port(), port(), binary()} | {error, any()}``

-  ``FilePath = string()``
-  ``Option = read_and_write | read | write``

put/3
~~~~~

``put(MetaDBId, StorageInfo, Object) -> {ok, integer()} | {error, any()}``

-  ``MetaDBId = atom()``
-  ``StorageInfo = #backend_info{}``
-  ``Object = #'?OBJECT'{}``

Insert an object and a metadata into the object-storage

put\_obj\_to\_new\_cntnr/4
~~~~~~~~~~~~~~~~~~~~~~~~~~

| ``put_obj_to_new_cntnr(WriteHandler::pid(), ?METADATA::#'?METADATA'{}, KeyBin::binary(), BodyBin::binary()) -> ok | {error, any()}``

Insert an object into the object-container when compacting

store/4
~~~~~~~

``store(MetaDBId, StorageInfo, Metadata, Bin) -> ok | {error, any()}``

-  ``MetaDBId = atom()``
-  ``StorageInfo = #backend_info{}``
-  ``Metadata = #'?METADATA'{}``
-  ``Bin = binary()``

Store metadata and binary
