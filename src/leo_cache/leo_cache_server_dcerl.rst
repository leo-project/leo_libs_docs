leo\_cache\_server\_dcerl
================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The disc-cache server.

**Behaviours:** ```leo_cache_behaviour`` <leo_cache_behaviour.html>`__.

**References**

-  ```https://github.com/leo-project/leo_cache/blob/master/src/leo_cache_server_dcerl.erl`` <https://github.com/leo-project/leo_cache/blob/master/src/leo_cache_server_dcerl.erl>`__

Description
-----------

The disc-cache server

Function Index
--------------

+----------------------------------------------+--------------------------------------------------------------+
| `delete/2 <#delete-2>`__                     | Remove an object from cache-server.                          |
+----------------------------------------------+--------------------------------------------------------------+
| `get/2 <#get-2>`__                           | Retrieve an object from cache-server.                        |
+----------------------------------------------+--------------------------------------------------------------+
| `get/3 <#get-3>`__                           | Retrieve an object from cache-server (for large-object).     |
+----------------------------------------------+--------------------------------------------------------------+
| `get\_filepath/2 <#get_filepath-2>`__        | Retrieve a meta data of cached object (for large-object).    |
+----------------------------------------------+--------------------------------------------------------------+
| `get\_ref/2 <#get_ref-2>`__                  | Retrieve a reference of cached object (for large-object).    |
+----------------------------------------------+--------------------------------------------------------------+
| `put/3 <#put-3>`__                           | Insert an object into cache-serverx.                         |
+----------------------------------------------+--------------------------------------------------------------+
| `put/4 <#put-4>`__                           | Insert an object into the cache-server (for large-object).   |
+----------------------------------------------+--------------------------------------------------------------+
| `put\_begin\_tran/2 <#put_begin_tran-2>`__   | Start put-transaction for large-object (for large-object).   |
+----------------------------------------------+--------------------------------------------------------------+
| `put\_end\_tran/5 <#put_end_tran-5>`__       | End put-transaction for large-object (for large-object).     |
+----------------------------------------------+--------------------------------------------------------------+
| `start/2 <#start-2>`__                       | Launch cache-server(s).                                      |
+----------------------------------------------+--------------------------------------------------------------+
| `stats/0 <#stats-0>`__                       | Retrieve status of this application.                         |
+----------------------------------------------+--------------------------------------------------------------+
| `stop/0 <#stop-0>`__                         | Stop cache-server(s).                                        |
+----------------------------------------------+--------------------------------------------------------------+

Function Details
----------------

delete/2
~~~~~~~~

``delete(Id, Key) -> ok | {error, any()}``

-  ``Id = integer()``
-  ``Key = binary() | any()``

Remove an object from cache-server

get/2
~~~~~

``get(Id, Key) -> not_found | {ok, binary()} | {error, any()}``

-  ``Id = integer()``
-  ``Key = binary() | any()``

Retrieve an object from cache-server

get/3
~~~~~

``get(Id, Ref, Key) -> not_found | {ok, binary()} | {error, any()}``

-  ``Id = integer()``
-  ``Ref = reference()``
-  ``Key = binary() | any()``

Retrieve an object from cache-server (for large-object)

get\_filepath/2
~~~~~~~~~~~~~~~

``get_filepath(Id, Key) -> {ok, #cache_meta{}} | {error, undefined}``

-  ``Id = integer()``
-  ``Key = binary() | any()``

Retrieve a meta data of cached object (for large-object)

get\_ref/2
~~~~~~~~~~

``get_ref(Id, Key) -> {ok, reference()} | {error, undefined}``

-  ``Id = integer()``
-  ``Key = binary() | any()``

Retrieve a reference of cached object (for large-object)

put/3
~~~~~

``put(Id, Key, Value) -> ok | {error, any()}``

-  ``Id = integer()``
-  ``Key = binary() | any()``
-  ``Value = binary() | any()``

Insert an object into cache-serverx

put/4
~~~~~

``put(Id, Ref, Key, Value) -> ok | {error, any()}``

-  ``Id = integer()``
-  ``Ref = reference()``
-  ``Key = binary() | any()``
-  ``Value = binary() | any()``

Insert an object into the cache-server (for large-object)

put\_begin\_tran/2
~~~~~~~~~~~~~~~~~~

``put_begin_tran(Id, Key) -> ok | {error, any()}``

-  ``Id = integer()``
-  ``Key = binary() | any()``

Start put-transaction for large-object (for large-object)

put\_end\_tran/5
~~~~~~~~~~~~~~~~

``put_end_tran(Id, Ref, Key, Meta, IsCommit) -> ok | {error, any()}``

-  ``Id = integer()``
-  ``Ref = reference()``
-  ``Key = binary() | any()``
-  ``Meta = #cache_meta{}``
-  ``IsCommit = boolean()``

End put-transaction for large-object (for large-object)

start/2
~~~~~~~

``start(Workers, Options) -> ok | {error, any()}``

-  ``Workers = integer()``
-  ``Options = [{atom(), any()}]``

Launch cache-server(s)

stats/0
~~~~~~~

| ``stats() -> {ok, any()} | {error, any()}``

Retrieve status of this application

stop/0
~~~~~~

| ``stop() -> ok``

Stop cache-server(s)
