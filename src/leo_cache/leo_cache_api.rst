leo\_cache\_api
======================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The cache API.

**References**

-  https://github.com/leo-project/leo\_cache/blob/master/src/leo\_cache\_server\_dcerl.erl

Description
-----------

The cache API

Function Index
--------------

+----------------------------------------------+-----------------------------------------------------------------+
| `delete/1 <#delete-1>`__                     | Remove an object from the momory storage.                       |
+----------------------------------------------+-----------------------------------------------------------------+
| `get/1 <#get-1>`__                           | Retrieve an object from the momory storage.                     |
+----------------------------------------------+-----------------------------------------------------------------+
| `get/2 <#get-2>`__                           | Retrieve a chunked-object from disc-cache (for large-object).   |
+----------------------------------------------+-----------------------------------------------------------------+
| `get\_filepath/1 <#get_filepath-1>`__        | Retrieve a meta data of cached object (for large-object).       |
+----------------------------------------------+-----------------------------------------------------------------+
| `get\_ref/1 <#get_ref-1>`__                  | Retrieve a reference of cached object (for large-object).       |
+----------------------------------------------+-----------------------------------------------------------------+
| `put/2 <#put-2>`__                           | Insert an object into the momory storage.                       |
+----------------------------------------------+-----------------------------------------------------------------+
| `put/3 <#put-3>`__                           | Insert a chunked-object into the disc.                          |
+----------------------------------------------+-----------------------------------------------------------------+
| `put\_begin\_tran/1 <#put_begin_tran-1>`__   | Insert a chunked-object into the disc.                          |
+----------------------------------------------+-----------------------------------------------------------------+
| `put\_end\_tran/4 <#put_end_tran-4>`__       | Insert a chunked-object into the disc.                          |
+----------------------------------------------+-----------------------------------------------------------------+
| `start/0 <#start-0>`__                       | Launch cache-server(s).                                         |
+----------------------------------------------+-----------------------------------------------------------------+
| `start/1 <#start-1>`__                       |                                                                 |
+----------------------------------------------+-----------------------------------------------------------------+
| `stats/0 <#stats-0>`__                       | Retrieve status of this application.                            |
+----------------------------------------------+-----------------------------------------------------------------+
| `stop/0 <#stop-0>`__                         | Stop cache-server(s).                                           |
+----------------------------------------------+-----------------------------------------------------------------+

Function Details
----------------

delete/1
~~~~~~~~

``delete(Key) -> ok | {error, any()}``

-  ``Key = binary()``

Remove an object from the momory storage

get/1
~~~~~

``get(Key) -> not_found | {ok, binary()} | {error, any()}``

-  ``Key = binary()``

Retrieve an object from the momory storage

get/2
~~~~~

``get(Ref, Key) -> not_found | {ok, {binary(), boolean()}} | {error, any()}``

-  ``Ref = reference()``
-  ``Key = binary()``

Retrieve a chunked-object from disc-cache (for large-object)

get\_filepath/1
~~~~~~~~~~~~~~~

``get_filepath(Key) -> not_found | {ok, #cache_meta{}} | {error, any()}``

-  ``Key = binary()``

Retrieve a meta data of cached object (for large-object)

get\_ref/1
~~~~~~~~~~

``get_ref(Key) -> not_found | {ok, reference()} | {error, any()}``

-  ``Key = binary()``

Retrieve a reference of cached object (for large-object)

put/2
~~~~~

``put(Key, Value) -> ok | {error, any()}``

-  ``Key = binary()``
-  ``Value = binary()``

Insert an object into the momory storage

put/3
~~~~~

``put(Ref, Key, Value) -> ok | {error, any()}``

-  ``Ref = reference()``
-  ``Key = binary()``
-  ``Value = binary()``

Insert a chunked-object into the disc

put\_begin\_tran/1
~~~~~~~~~~~~~~~~~~

``put_begin_tran(Key) -> {ok, reference()} | {error, any()}``

-  ``Key = binary()``

Insert a chunked-object into the disc

put\_end\_tran/4
~~~~~~~~~~~~~~~~

``put_end_tran(Ref, Key, Meta, IsCommit) -> {ok, reference()} | {error, any()}``

-  ``Ref = reference()``
-  ``Key = binary()``
-  ``Meta = #cache_meta{}``
-  ``IsCommit = boolean()``

Insert a chunked-object into the disc

start/0
~~~~~~~

| ``start() -> ok | {error, any()}``

Launch cache-server(s)

start/1
~~~~~~~

``start(Options) -> ok | {error, any()}``

-  ``Options = [{atom(), any()}]``

stats/0
~~~~~~~

| ``stats() -> {ok, any()}``

Retrieve status of this application

stop/0
~~~~~~

| ``stop() -> ok``

Stop cache-server(s)
