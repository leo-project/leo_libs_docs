leo\_rpc\_client\_conn
=============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_rpc\_client\_conn is a rpc-client.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  ```https://github.com/leo-project/leo_rpc/blob/master/src/leo_rpc_client_conn`` <https://github.com/leo-project/leo_rpc/blob/master/src/leo_rpc_client_conn>`__

Description
-----------

leo\_rpc\_client\_conn is a rpc-client

Function Index
--------------

+---------------------------------------+----------------------------------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__   | gen\_server callback - Module:code\_change(OldVsn, State, Extra) -> {ok, NewState} \| {error, Reason}.   |
+---------------------------------------+----------------------------------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__   | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.                              |
+---------------------------------------+----------------------------------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__   | gen\_server callback - Module:handle\_cast(Request, State) -> Result.                                    |
+---------------------------------------+----------------------------------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__   | gen\_server callback - Module:handle\_info(Info, State) -> Result.                                       |
+---------------------------------------+----------------------------------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                  | gen\_server callback - Module:init(Args) -> Result.                                                      |
+---------------------------------------+----------------------------------------------------------------------------------------------------------+
| `start\_link/1 <#start_link-1>`__     | Start the server.                                                                                        |
+---------------------------------------+----------------------------------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                  | Stop the server.                                                                                         |
+---------------------------------------+----------------------------------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__        | gen\_server callback - Module:terminate(Reason, State).                                                  |
+---------------------------------------+----------------------------------------------------------------------------------------------------------+

Function Details
----------------

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

gen\_server callback - Module:code\_change(OldVsn, State, Extra) -> {ok,
NewState} \| {error, Reason}

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

start\_link/1
~~~~~~~~~~~~~

| ``start_link(X1::[any()]) -> {ok, pid()} | {error, term()}``

Start the server

stop/1
~~~~~~

| ``stop(ServerRef::pid()) -> ok | {error, any()}``

Stop the server

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

gen\_server callback - Module:terminate(Reason, State)
