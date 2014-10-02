leo\_dcerl\_server
=========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The disc cache's server.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

Description
-----------

The disc cache's server

Function Index
--------------

+----------------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__          | Convert process state when code is changed.                                   |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `delete/2 <#delete-2>`__                     | Remove a key-value pair by a specified key into the leo\_dcerl.               |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `get/2 <#get-2>`__                           | Retrieve a value associated with a specified key.                             |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `get/3 <#get-3>`__                           | Retrieve a value associated with a specified key.                             |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `get\_filepath/2 <#get_filepath-2>`__        | Retrieve a value associated with a specified key.                             |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `get\_ref/2 <#get_ref-2>`__                  | Retrieve a reference.                                                         |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__          | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.   |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__          | Handling cast message.                                                        |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__          | Handling all non call/cast messages.                                          |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                         | Initiates the server.                                                         |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `items/1 <#items-1>`__                       | Return server's items.                                                        |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `put/3 <#put-3>`__                           | Insert a key-value pair into the leo\_dcerl.                                  |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `put/4 <#put-4>`__                           |                                                                               |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `put\_begin\_tran/2 <#put_begin_tran-2>`__   | Start transaction of insert chunked objects.                                  |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `put\_end\_tran/5 <#put_end_tran-5>`__       | End transaction of insert chunked objects.                                    |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `size/1 <#size-1>`__                         | Return server's summary of cache size.                                        |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/5 <#start_link-5>`__            | Starts the server.                                                            |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `stats/1 <#stats-1>`__                       | Return server's state.                                                        |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                         | Manually stops the server.                                                    |
+----------------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__               | This function is called by a gen\_server when it is about to terminate.       |
+----------------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

delete/2
~~~~~~~~

``delete(Id, Key) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Key = binary()``

Remove a key-value pair by a specified key into the leo\_dcerl

get/2
~~~~~

``get(Id, Key) -> undefined | binary() | {error, any()}``

-  ``Id = atom()``
-  ``Key = binary()``

Retrieve a value associated with a specified key

get/3
~~~~~

``get(Id, Ref, Key) -> undefined | binary() | {error, any()}``

-  ``Id = atom()``
-  ``Ref = any()``
-  ``Key = binary()``

Retrieve a value associated with a specified key

get\_filepath/2
~~~~~~~~~~~~~~~

``get_filepath(Id, Key) -> undefined | #cache_meta{} | {error, any()}``

-  ``Id = atom()``
-  ``Key = binary()``

Retrieve a value associated with a specified key

get\_ref/2
~~~~~~~~~~

``get_ref(Id, Key) -> undefined | binary() | {error, any()}``

-  ``Id = atom()``
-  ``Key = binary()``

Retrieve a reference

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(Request, From, State) -> any()``

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

init/1
~~~~~~

``init(X1) -> any()``

Initiates the server

items/1
~~~~~~~

``items(Id) -> any()``

-  ``Id = atom()``

Return server's items

put/3
~~~~~

``put(Id, Key, Value) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Key = binary()``
-  ``Value = binary()``

Insert a key-value pair into the leo\_dcerl

put/4
~~~~~

``put(Id, Ref, Key, Value) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Ref = any()``
-  ``Key = binary()``
-  ``Value = binary()``

put\_begin\_tran/2
~~~~~~~~~~~~~~~~~~

``put_begin_tran(Id, Key) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Key = binary()``

Start transaction of insert chunked objects

put\_end\_tran/5
~~~~~~~~~~~~~~~~

``put_end_tran(Id, Ref, Key, Meta, IsCommit) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Ref = any()``
-  ``Key = binary()``
-  ``Meta = #cache_meta{}``
-  ``IsCommit = boolean()``

End transaction of insert chunked objects

size/1
~~~~~~

``size(Id) -> any()``

-  ``Id = atom()``

Return server's summary of cache size

start\_link/5
~~~~~~~~~~~~~

``start_link(Id, DataDir, JournalDir, CacheSize, ChunkSize) -> ignore | {error, term()} | {ok, pid()}``

-  ``Id = atom()``
-  ``DataDir = string()``
-  ``JournalDir = string()``
-  ``CacheSize = integer()``
-  ``ChunkSize = integer()``

Starts the server.

stats/1
~~~~~~~

``stats(Id) -> any()``

-  ``Id = atom()``

Return server's state

stop/1
~~~~~~

``stop(Pid) -> ok``

-  ``Pid = atom()``

Manually stops the server.

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason.
