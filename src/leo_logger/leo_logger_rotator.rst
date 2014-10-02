leo\_logger\_rotator
===========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The log rotator.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  https://github.com/leo-project/leo\_logger/blob/master/src/leo\_logger\_rotator.erl

Description
-----------

The log rotator

Function Index
--------------

+---------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__   | Convert process state when code is changed.                                   |
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
| `start\_link/3 <#start_link-3>`__     |                                                                               |
+---------------------------------------+-------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                  | Stop the server.                                                              |
+---------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__        | This function is called by a gen\_server when it is about to terminate.       |
+---------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(Request, From, State) -> any()``

gen\_server callback - Module:handle\_call(Request, From, State) ->
Result

handle\_cast/2
~~~~~~~~~~~~~~

``handle_cast(Msg, State) -> any()``

Handling cast message

gen\_server callback - Module:handle\_cast(Request, State) -> Result.

handle\_info/2
~~~~~~~~~~~~~~

``handle_info(X1, State) -> any()``

Handling all non call/cast messages

gen\_server callback - Module:handle\_info(Info, State) -> Result.

init/1
~~~~~~

``init(X1) -> any()``

Initiates the server

start\_link/2
~~~~~~~~~~~~~

``start_link(ServerId, Mod) -> {ok, pid()} | ignore | {error, any()}``

-  ``ServerId = atom()``
-  ``Mod = module()``

Start the server

start\_link/3
~~~~~~~~~~~~~

``start_link(ServerId, Mod, RotationInterval) -> {ok, pid()} | ignore | {error, any()}``

-  ``ServerId = atom()``
-  ``Mod = atom()``
-  ``RotationInterval = pos_integer()``

stop/1
~~~~~~

``stop(Pid) -> ok``

-  ``Pid = pid()``

Stop the server

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason.
