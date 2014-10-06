+----------------------------------------+-----------------+
| `Overview <overview-summary.html>`__   | |erlang logo|   |
+----------------------------------------+-----------------+

--------------

Module leo\_ordning\_reda\_server
=================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The ordning-reda server.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  ```https://github.com/leo-project/leo_ordning_reda/blob/master/src/leo_ordning_reda_server.erl`` <https://github.com/leo-project/leo_ordning_reda/blob/master/src/leo_ordning_reda_server.erl>`__

Description
-----------

The ordning-reda server

Function Index
--------------

+---------------------------------------+-------------------------------------------------------------------------------+
| `close/1 <#close-1>`__                | Close a stacked file.                                                         |
+---------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__   | Convert process state when code is changed.                                   |
+---------------------------------------+-------------------------------------------------------------------------------+
| `exec/1 <#exec-1>`__                  | Send stacked objects to remote-node(s).                                       |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__   | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.   |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__   | Handling cast message.                                                        |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__   | Handling all non call/cast messages.                                          |
+---------------------------------------+-------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                  | Initiates the server.                                                         |
+---------------------------------------+-------------------------------------------------------------------------------+
| `stack/3 <#stack-3>`__                | Stack objects.                                                                |
+---------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/2 <#start_link-2>`__     | Start the server.                                                             |
+---------------------------------------+-------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                  | Stop this server.                                                             |
+---------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__        | This function is called by a gen\_server when it is about to terminate.       |
+---------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

close/1
~~~~~~~

``close(Id) -> ok | {error, any()}``

-  ``Id = atom()``

Close a stacked file

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

exec/1
~~~~~~

``exec(Id) -> ok | {error, any()}``

-  ``Id = atom()``

Send stacked objects to remote-node(s).

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(X1, From, State) -> any()``

gen\_server callback - Module:handle\_call(Request, From, State) ->
Result

handle\_cast/2
~~~~~~~~~~~~~~

``handle_cast(Msg, State) -> any()``

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

stack/3
~~~~~~~

``stack(Id, StrawId, ObjBin) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``StrawId = any()``
-  ``ObjBin = binary()``

Stack objects

start\_link/2
~~~~~~~~~~~~~

``start_link(Id, StackInfo) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``StackInfo = #stack_info{}``

Start the server

stop/1
~~~~~~

``stop(Id) -> ok``

-  ``Id = atom()``

Stop this server

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason.

--------------

+----------------------------------------+-----------------+
| `Overview <overview-summary.html>`__   | |erlang logo|   |
+----------------------------------------+-----------------+

*Generated by EDoc, Oct 6 2014, 09:48:16.*

.. |erlang logo| image:: erlang.png
   :target: http://www.erlang.org/
