leo\_rpc
===============

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_rpc is an original RPC library whose interface is similar to
Erlang's buildin RPC.

**References**

-  ```https://github.com/leo-project/leo_rpc/blob/develop/master/leo_rpc.erl`` <https://github.com/leo-project/leo_rpc/blob/develop/master/leo_rpc.erl>`__

Description
-----------

leo\_rpc is an original RPC library whose interface is similar to
Erlang's buildin RPC.

Function Index
--------------

+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `async\_call/4 <#async_call-4>`__   | Implements call streams with promises, a type of RPC which does not suspend the caller until the result is finished.                       |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `call/4 <#call-4>`__                | Evaluates apply(Module, Function, Args) on the node Node and returns the corresponding value Res, or {badrpc, Reason} if the call fails.   |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `call/5 <#call-5>`__                | Evaluates apply(Module, Function, Args) on the node Node and returns the corresponding value Res, or {badrpc, Reason} if the call fails.   |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `call/6 <#call-6>`__                | Evaluates apply(Module, Function, Args) on the node Node and returns the corresponding value Res, or {badrpc, Reason} if the call fails.   |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `cast/4 <#cast-4>`__                | No response is delivered and the calling process is not suspended until the evaluation is complete, as is the case with call/4,5.          |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `multicall/4 <#multicall-4>`__      | A multicall is an RPC which is sent concurrently from one client to multiple servers.                                                      |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `multicall/5 <#multicall-5>`__      | A multicall is an RPC which is sent concurrently from one client to multiple servers.                                                      |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `nb\_yield/1 <#nb_yield-1>`__       | This is able to call non-blocking.                                                                                                         |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `nb\_yield/2 <#nb_yield-2>`__       | This is able to call non-blocking.                                                                                                         |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `node/0 <#node-0>`__                | Returns the name of the local node.                                                                                                        |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `nodes/0 <#nodes-0>`__              | Returns a list of all connected nodes in the system, excluding the local node.                                                             |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `ping/1 <#ping-1>`__                | Tries to set up a connection to Node.                                                                                                      |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `port/0 <#port-0>`__                | Returns the port number of the local node.                                                                                                 |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `start/0 <#start-0>`__              | Launch leo-rpc.                                                                                                                            |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
| `status/0 <#status-0>`__            | Retrieve status of active connections.                                                                                                     |
+-------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+

Function Details
----------------

async\_call/4
~~~~~~~~~~~~~

``async_call(Node, Mod, Method, Args) -> pid()``

-  ``Node = atom()``
-  ``Mod = module()``
-  ``Method = atom()``
-  ``Args = [any()]``

Implements call streams with promises, a type of RPC which does not
suspend the caller until the result is finished. Instead, a key is
returned which can be used at a later stage to collect the value. The
key can be viewed as a promise to deliver the answer.

call/4
~~~~~~

``call(Node, Mod, Method, Args) -> Ret | {badrpc, any()}``

-  ``Node = atom()``
-  ``Mod = module()``
-  ``Method = atom()``
-  ``Args = [any()]``
-  ``Ret = any()``

Evaluates apply(Module, Function, Args) on the node Node and returns the
corresponding value Res, or {badrpc, Reason} if the call fails.

call/5
~~~~~~

``call(Node, Mod, Method, Args, Timeout) -> Ret | {badrpc, any()}``

-  ``Node = atom()``
-  ``Mod = module()``
-  ``Method = atom()``
-  ``Args = [any()]``
-  ``Timeout = pos_integer()``
-  ``Ret = any()``

Evaluates apply(Module, Function, Args) on the node Node and returns the
corresponding value Res, or {badrpc, Reason} if the call fails.

call/6
~~~~~~

``call(From, Node, Mod, Method, Args, Timeout) -> Ret | {badrpc, any()}``

-  ``From = pid()``
-  ``Node = atom()``
-  ``Mod = module()``
-  ``Method = atom()``
-  ``Args = [any()]``
-  ``Timeout = pos_integer()``
-  ``Ret = any()``

Evaluates apply(Module, Function, Args) on the node Node and returns the
corresponding value Res, or {badrpc, Reason} if the call fails.

cast/4
~~~~~~

``cast(Node, Mod, Method, Args) -> true``

-  ``Node = atom()``
-  ``Mod = module()``
-  ``Method = atom()``
-  ``Args = [any()]``

No response is delivered and the calling process is not suspended until
the evaluation is complete, as is the case with call/4,5.

multicall/4
~~~~~~~~~~~

``multicall(Nodes, Mod, Method, Args) -> Ret | {badrpc, any()}``

-  ``Nodes = [atom()]``
-  ``Mod = module()``
-  ``Method = atom()``
-  ``Args = [any()]``
-  ``Ret = any()``

A multicall is an RPC which is sent concurrently from one client to
multiple servers. This is useful for collecting some information from a
set of nodes.

multicall/5
~~~~~~~~~~~

``multicall(Nodes, Mod, Method, Args, Timeout) -> Ret | {badrpc, any()}``

-  ``Nodes = [atom()]``
-  ``Mod = module()``
-  ``Method = atom()``
-  ``Args = [any()]``
-  ``Timeout = pos_integer()``
-  ``Ret = [any()]``

A multicall is an RPC which is sent concurrently from one client to
multiple servers. This is useful for collecting some information from a
set of nodes.

nb\_yield/1
~~~~~~~~~~~

``nb_yield(Key) -> {value, any()} | timeout``

-  ``Key = pid()``

This is able to call non-blocking. It returns the tuple {value, Val}
when the computation has finished, or timeout when Timeout milliseconds
has elapsed.

nb\_yield/2
~~~~~~~~~~~

``nb_yield(Key, Timeout) -> {value, any()} | timeout``

-  ``Key = pid()``
-  ``Timeout = pos_integer()``

This is able to call non-blocking. It returns the tuple {value, Val}
when the computation has finished, or timeout when Timeout milliseconds
has elapsed.

node/0
~~~~~~

``node() -> Node``

-  ``Node = atom()``

Returns the name of the local node. The default name is
``nonode@nohost``.

nodes/0
~~~~~~~

``nodes() -> Nodes``

-  ``Nodes = [atom()]``

Returns a list of all connected nodes in the system, excluding the local
node.

ping/1
~~~~~~

``ping(Node) -> pong | pang``

-  ``Node = atom()``

Tries to set up a connection to Node. Returns pang if it fails, or pong
if it is successful.

port/0
~~~~~~

| ``port() -> pos_integer()``

Returns the port number of the local node.

start/0
~~~~~~~

| ``start() -> ok | {error, any()}``

Launch leo-rpc

status/0
~~~~~~~~

| ``status() -> {ok, [#rpc_info{}]} | {error, any()}``

Retrieve status of active connections.
