leo\_mdcr\_tbl\_sync
===========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The multi-datacenter cluster talble synchronizer.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  ```https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_mdcr_tbl_sync.erl`` <https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_mdcr_tbl_sync.erl>`__

Description
-----------

The multi-datacenter cluster talble synchronizer

Function Index
--------------

+---------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__   | Convert process state when code is changed.                                   |
+---------------------------------------+-------------------------------------------------------------------------------+
| `force\_sync/0 <#force_sync-0>`__     | Force the records synchronize with the remote cluster(s).                     |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__   | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.   |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__   | Handling cast message.                                                        |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__   | Handling all non call/cast messages.                                          |
+---------------------------------------+-------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                  | Initiates the server.                                                         |
+---------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/2 <#start_link-2>`__     | Start the server.                                                             |
+---------------------------------------+-------------------------------------------------------------------------------+
| `stop/0 <#stop-0>`__                  | Stop the server.                                                              |
+---------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__        | This function is called by a gen\_server when it is about to terminate.       |
+---------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

force\_sync/0
~~~~~~~~~~~~~

``force_sync() -> any()``

Force the records synchronize with the remote cluster(s)

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(X1, From, State) -> any()``

gen\_server callback - Module:handle\_call(Request, From, State) ->
Result

handle\_cast/2
~~~~~~~~~~~~~~

``handle_cast(X1, State) -> any()``

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

start\_link/2
~~~~~~~~~~~~~

``start_link(ServerType, Managers) -> any()``

Start the server

stop/0
~~~~~~

``stop() -> any()``

Stop the server

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason.
