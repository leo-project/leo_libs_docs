leo\_rpc\_server
=======================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_rpc\_server is a rpc-server.

**References**

- https://github.com/leo-project/leo_rpc/blob/master/src/leo_rpc_server.erl

Description
-----------

leo\_rpc\_server is a rpc-server

Function Index
--------------

+-------------------------------------+-----------------------------------------+
| `start\_link/3 <#start_link-3>`__   | Start tcp-listener of the rpc-server.   |
+-------------------------------------+-----------------------------------------+
| `stop/0 <#stop-0>`__                | Stop tcp-listener(s).                   |
+-------------------------------------+-----------------------------------------+

Function Details
----------------

start\_link/3
~~~~~~~~~~~~~

``start_link(Module, Args, Option) -> ok | {error, any()}``

-  ``Module = module()``
-  ``Args = [any()]``
-  ``Option = #tcp_server_params{}``

Start tcp-listener of the rpc-server

stop/0
~~~~~~

| ``stop() -> ok``

Stop tcp-listener(s)
