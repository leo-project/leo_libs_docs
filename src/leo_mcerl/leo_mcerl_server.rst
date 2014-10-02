leo\_mcerl\_server
=========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The memory cache server.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  https://github.com/leo-project/leo\_mcerl/blob/master/src/leo\_mcerl\_server.erl

Description
-----------

The memory cache server

Function Index
--------------

+---------------------------------------+-------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__   |                                                                   |
+---------------------------------------+-------------------------------------------------------------------+
| `delete/2 <#delete-2>`__              | Remove a key-value pair by a specified key into the leo\_mcerl.   |
+---------------------------------------+-------------------------------------------------------------------+
| `get/2 <#get-2>`__                    | Retrieve a value associated with a specified key.                 |
+---------------------------------------+-------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__   |                                                                   |
+---------------------------------------+-------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__   |                                                                   |
+---------------------------------------+-------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__   |                                                                   |
+---------------------------------------+-------------------------------------------------------------------+
| `init/1 <#init-1>`__                  |                                                                   |
+---------------------------------------+-------------------------------------------------------------------+
| `items/1 <#items-1>`__                | Return server's items.                                            |
+---------------------------------------+-------------------------------------------------------------------+
| `put/3 <#put-3>`__                    | Insert a key-value pair into the leo\_mcerl.                      |
+---------------------------------------+-------------------------------------------------------------------+
| `size/1 <#size-1>`__                  | Return server's summary of cache size.                            |
+---------------------------------------+-------------------------------------------------------------------+
| `start\_link/2 <#start_link-2>`__     | Start the server.                                                 |
+---------------------------------------+-------------------------------------------------------------------+
| `stats/1 <#stats-1>`__                | Return server's state.                                            |
+---------------------------------------+-------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                  | Stop the server.                                                  |
+---------------------------------------+-------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__        |                                                                   |
+---------------------------------------+-------------------------------------------------------------------+

Function Details
----------------

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

delete/2
~~~~~~~~

``delete(Id, Key) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Key = binary()``

Remove a key-value pair by a specified key into the leo\_mcerl

get/2
~~~~~

``get(Id, Key) -> undefined | binary() | {error, any()}``

-  ``Id = atom()``
-  ``Key = binary()``

Retrieve a value associated with a specified key

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(Request, From, State) -> any()``

handle\_cast/2
~~~~~~~~~~~~~~

``handle_cast(Msg, State) -> any()``

handle\_info/2
~~~~~~~~~~~~~~

``handle_info(Info, State) -> any()``

init/1
~~~~~~

``init(X1) -> any()``

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

Insert a key-value pair into the leo\_mcerl

size/1
~~~~~~

``size(Id) -> any()``

-  ``Id = atom()``

Return server's summary of cache size

start\_link/2
~~~~~~~~~~~~~

``start_link(Id, CacheSize) -> {ok, pid()} | ignore | {error, any()}``

-  ``Id = atom()``
-  ``CacheSize = non_neg_integer()``

Start the server

stats/1
~~~~~~~

``stats(Id) -> any()``

-  ``Id = atom()``

Return server's state

stop/1
~~~~~~

``stop(Id) -> ok``

-  ``Id = atom()``

Stop the server

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``
