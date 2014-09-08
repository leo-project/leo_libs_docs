leo\_rpc\_protocol
=========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_rpc\_protocol handles requested data with the protocol.

**References**

- https://github.com/leo-project/leo_rpc/blob/master/src/leo_rpc_protocol.erl

Description
-----------

leo\_rpc\_protocol handles requested data with the protocol

Function Index
--------------

+--------------------------------------------------+------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__              | Receive data from client(s) after that convert from param to binary.   |
+--------------------------------------------------+------------------------------------------------------------------------+
| `init/1 <#init-1>`__                             | Initialize the protocol.                                               |
+--------------------------------------------------+------------------------------------------------------------------------+
| `param\_to\_binary/3 <#param_to_binary-3>`__     | Convert from param to binary.                                          |
+--------------------------------------------------+------------------------------------------------------------------------+
| `result\_to\_binary/1 <#result_to_binary-1>`__   | Convert from result-value to binary.                                   |
+--------------------------------------------------+------------------------------------------------------------------------+
| `start\_link/0 <#start_link-0>`__                | Start leo\_rpc's server.                                               |
+--------------------------------------------------+------------------------------------------------------------------------+
| `start\_link/1 <#start_link-1>`__                | Start leo\_rpc's server.                                               |
+--------------------------------------------------+------------------------------------------------------------------------+
| `stop/0 <#stop-0>`__                             | Stop leo\_rpc's server.                                                |
+--------------------------------------------------+------------------------------------------------------------------------+

Function Details
----------------

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(Socket, Data, State) -> {reply, binary()} | {close, State}``

-  ``Socket = gen_tcp:socket()``
-  ``Data = binary()``
-  ``State = any()``

Receive data from client(s) after that convert from param to binary

::

      dat-format:
      << "*",
         $ModMethodBin/binary,    "/r/n",
         $ParamsLenBin:8/integer, $BodyLen:32/integer, "/r/n",
         $Param_1_Bin_Len/binary, "/r/n", "T"|"B", $Param_1_Bin/binary, "/r/n",
         ...
         $Param_N_Bin_Len/binary, "/r/n", "T"|"B", $Param_N_Bin/binary, "/r/n",
         "/r/n" >>
      

init/1
~~~~~~

| ``init(X1::term()) -> {ok, null}``

Initialize the protocol

param\_to\_binary/3
~~~~~~~~~~~~~~~~~~~

``param_to_binary(Mod, Method, Args) -> binary()``

-  ``Mod = module()``
-  ``Method = atom()``
-  ``Args = [any()]``

Convert from param to binary

::

      Format:
      << "*",
         $ModMethodBin/binary,    "/r/n",
         $ParamsLenBin:8/integer, $BodyLen:32/integer, "/r/n",
         $Param_1_Bin_Len/binary, "/r/n", "T"|"B", $Param_1_Bin/binary, "/r/n",
         ...
         $Param_N_Bin_Len/binary, "/r/n", "T"|"B", $Param_N_Bin/binary, "/r/n",
         "/r/n" >>
      

result\_to\_binary/1
~~~~~~~~~~~~~~~~~~~~

``result_to_binary(Term) -> binary()``

-  ``Term = any()``

Convert from result-value to binary

::

      Format:
      << "*",
         $OriginalDataTypeBin/binary, ResultBodyLen/integer, "/r/n",
         $BodyBin_1_Len/integer,      "/r/n",
         $BodyBin_1/binary,           "/r/n",
         ...
         $BodyBin_N_Len/integer,      "/r/n",
         $BodyBin_N/binary,           "/r/n",
         "/r/n"
         >>
      

start\_link/0
~~~~~~~~~~~~~

| ``start_link() -> ok | {error, any()}``

Start leo\_rpc's server

start\_link/1
~~~~~~~~~~~~~

``start_link(Params) -> ok | {error, any()}``

-  ``Params = #tcp_server_params{}``

Start leo\_rpc's server

stop/0
~~~~~~

| ``stop() -> ok | {error, any()}``

Stop leo\_rpc's server
