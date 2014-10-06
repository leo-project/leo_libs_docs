leo\_rpc\_client\_manager
================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_rpc\_client\_conn\_manager manages rpc-clients.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  https://github.com/leo-project/leo\_rpc/blob/master/src/leo\_rpc\_client\_manager

Description
-----------

leo\_rpc\_client\_conn\_manager manages rpc-clients

Function Index
--------------

+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__           | gen\_server callback - Module:code\_change(OldVsn, State, Extra) -> {ok, NewState} \| {error, Reason}.   |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `connected\_nodes/0 <#connected_nodes-0>`__   | Retrieve connected nodes.                                                                                |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__           | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.                              |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__           | gen\_server callback - Module:handle\_cast(Request, State) -> Result.                                    |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__           | gen\_server callback - Module:handle\_info(Info, State) -> Result.                                       |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                          | gen\_server callback - Module:init(Args) -> Result.                                                      |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `inspect/0 <#inspect-0>`__                    | Inspect whether a node is running or not.                                                                |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `inspect/1 <#inspect-1>`__                    | Inspect whether the node is running or not.                                                              |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `is\_exists/2 <#is_exists-2>`__               | Is already ip/port exists.                                                                               |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `start\_link/1 <#start_link-1>`__             | Start the server.                                                                                        |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `status/0 <#status-0>`__                      | Retrieve the current status.                                                                             |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `stop/0 <#stop-0>`__                          | Stop the server.                                                                                         |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__                | gen\_server callback - Module:terminate(Reason, State).                                                  |
+-----------------------------------------------+----------------------------------------------------------------------------------------------------------+

Function Details
----------------

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

gen\_server callback - Module:code\_change(OldVsn, State, Extra) -> {ok,
NewState} \| {error, Reason}.

connected\_nodes/0
~~~~~~~~~~~~~~~~~~

| ``connected_nodes() -> {ok, [atom()]}``

Retrieve connected nodes

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(Request, From, State) -> any()``

gen\_server callback - Module:handle\_call(Request, From, State) ->
Result

handle\_cast/2
~~~~~~~~~~~~~~

``handle_cast(Msg, State) -> any()``

gen\_server callback - Module:handle\_cast(Request, State) -> Result

handle\_info/2
~~~~~~~~~~~~~~

``handle_info(Info, State) -> any()``

gen\_server callback - Module:handle\_info(Info, State) -> Result

init/1
~~~~~~

``init(X1) -> any()``

gen\_server callback - Module:init(Args) -> Result

inspect/0
~~~~~~~~~

| ``inspect() -> ok``

Inspect whether a node is running or not

inspect/1
~~~~~~~~~

``inspect(Node) -> active | inactive``

-  ``Node = atom()``

Inspect whether the node is running or not

is\_exists/2
~~~~~~~~~~~~

``is_exists(IP, Port) -> boolean()``

-  ``IP = string()``
-  ``Port = pos_integer()``

Is already ip/port exists

start\_link/1
~~~~~~~~~~~~~

``start_link(Interval) -> {ok, pid()} | {error, term()}``

-  ``Interval = pos_integer()``

Start the server

status/0
~~~~~~~~

| ``status() -> {ok, [tuple()]}``

Retrieve the current status

stop/0
~~~~~~

| ``stop() -> ok``

Stop the server

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

gen\_server callback - Module:terminate(Reason, State)
