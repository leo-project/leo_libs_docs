leo\_membership\_cluster\_local
======================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The membership operation in the local-cluster.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  ```https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_membership_cluster_local.erl`` <https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_membership_cluster_local.erl>`__

Description
-----------

The membership operation in the local-cluster

Function Index
--------------

+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__                      | Convert process state when code is changed.                                   |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__                      | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.   |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__                      | Handling cast message.                                                        |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__                      | Handling all non call/cast messages.                                          |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `heartbeat/0 <#heartbeat-0>`__                           | Start the heartbeat operation.                                                |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                                     | Initiates the server.                                                         |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `set\_proc\_auditor/1 <#set_proc_auditor-1>`__           | Set the process of an auditor.                                                |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `start\_heartbeat/0 <#start_heartbeat-0>`__              | Start the heartbeat operation.                                                |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/2 <#start_link-2>`__                        | Start the server.                                                             |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/3 <#start_link-3>`__                        |                                                                               |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `stop/0 <#stop-0>`__                                     | Stop the server.                                                              |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `stop\_heartbeat/0 <#stop_heartbeat-0>`__                | Stop the heartbeat operation.                                                 |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__                           | This function is called by a gen\_server when it is about to terminate.       |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `update\_manager\_nodes/1 <#update_manager_nodes-1>`__   | Update the manager nodes.                                                     |
+----------------------------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

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

set\_proc\_auditor/1
~~~~~~~~~~~~~~~~~~~~

``set_proc_auditor(ProcAuditor) -> ok | {error, any()}``

-  ``ProcAuditor = atom()``

Set the process of an auditor

start\_heartbeat/0
~~~~~~~~~~~~~~~~~~

| ``start_heartbeat() -> ok | {error, any()}``

Start the heartbeat operation

start\_link/2
~~~~~~~~~~~~~

``start_link(ServerType, Managers) -> {ok, pid()} | {error, any()}``

-  ``ServerType = atom()``
-  ``Managers = [atom()]``

Start the server

start\_link/3
~~~~~~~~~~~~~

``start_link(ServerType, Managers, Callback) -> {ok, pid()} | {error, any()}``

-  ``ServerType = atom()``
-  ``Managers = [atom()]``
-  ``Callback = function()``

stop/0
~~~~~~

``stop() -> any()``

Stop the server

stop\_heartbeat/0
~~~~~~~~~~~~~~~~~

| ``stop_heartbeat() -> ok | {error, any()}``

Stop the heartbeat operation

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason.

update\_manager\_nodes/1
~~~~~~~~~~~~~~~~~~~~~~~~

``update_manager_nodes(Managers) -> ok | {error, any()}``

-  ``Managers = [atom()]``

Update the manager nodes
