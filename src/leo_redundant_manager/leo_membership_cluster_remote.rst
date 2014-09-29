leo\_membership\_cluster\_remote
=======================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The membership operation with remote-cluster(s).

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  ```https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_membership_cluster_remote.erl`` <https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_membership_cluster_remote.erl>`__

Description
-----------

The membership operation with remote-cluster(s)

Function Index
--------------

+---------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__   | Convert process state when code is changed.                                   |
+---------------------------------------+-------------------------------------------------------------------------------+
| `force\_sync/2 <#force_sync-2>`__     | Force the info to synchronize with the remote-cluster(s).                     |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__   | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.   |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__   | Handling cast message.                                                        |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__   | Handling all non call/cast messages.                                          |
+---------------------------------------+-------------------------------------------------------------------------------+
| `heartbeat/0 <#heartbeat-0>`__        | Start the heartbeat operation.                                                |
+---------------------------------------+-------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                  | Initiates the server.                                                         |
+---------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/0 <#start_link-0>`__     | Start the server.                                                             |
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

force\_sync/2
~~~~~~~~~~~~~

``force_sync(ClusterId, RemoteManagers) -> ok``

-  ``ClusterId = atom()``
-  ``RemoteManagers = [atom()]``

Force the info to synchronize with the remote-cluster(s)

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

heartbeat/0
~~~~~~~~~~~

| ``heartbeat() -> ok | {error, any()}``

Start the heartbeat operation

init/1
~~~~~~

``init(X1) -> any()``

Initiates the server

start\_link/0
~~~~~~~~~~~~~

``start_link() -> any()``

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
