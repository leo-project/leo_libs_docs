leo\_rpc\_server\_listener
=================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_rpc\_server\_listener is a rpc-server's listener.

**References**

- https://github.com/leo-project/leo_rpc/blob/master/src/leo_rpc_server_listener.erl

Description
-----------

leo\_rpc\_server\_listener is a rpc-server's listener

Function Index
--------------

+-------------------------------------+----------------------------------------+
| `accept/5 <#accept-5>`__            | Callback - Accept the communication.   |
+-------------------------------------+----------------------------------------+
| `init/5 <#init-5>`__                | Callback - Initialize the server.      |
+-------------------------------------+----------------------------------------+
| `start\_link/5 <#start_link-5>`__   | Start a rpc-server's listener.         |
+-------------------------------------+----------------------------------------+

Function Details
----------------

accept/5
~~~~~~~~

``accept(ListenSocket, State, Module, Active, Options) -> ok``

-  ``ListenSocket = gen_tcp:socket()``
-  ``State = any()``
-  ``Module = module()``
-  ``Active = boolean()``
-  ``Options = #tcp_server_params{}``

Callback - Accept the communication

init/5
~~~~~~

``init(Parent, Socket, State, Module, Options) -> ok``

-  ``Parent = pid()``
-  ``Socket = gen_tcp:socket()``
-  ``State = any()``
-  ``Module = module()``
-  ``Options = #tcp_server_params{}``

Callback - Initialize the server

start\_link/5
~~~~~~~~~~~~~

``start_link(Id, Socket, State, Module, Options) -> {ok, pid()}``

-  ``Id = {atom(), atom()}``
-  ``Socket = pid()``
-  ``State = atom()``
-  ``Module = module()``
-  ``Options = #tcp_server_params{}``

Start a rpc-server's listener
