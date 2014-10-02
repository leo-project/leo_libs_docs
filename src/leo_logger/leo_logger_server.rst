leo\_logger\_server
==========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The log server.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  https://github.com/leo-project/leo\_logger/blob/master/src/leo\_logger\_server.erl

Description
-----------

The log server

Function Index
--------------

+---------------------------------------+-------------------------------------------------------------------------------+
| `append/3 <#append-3>`__              | Append a message to a log-file.                                               |
+---------------------------------------+-------------------------------------------------------------------------------+
| `append/4 <#append-4>`__              |                                                                               |
+---------------------------------------+-------------------------------------------------------------------------------+
| `bulk\_output/1 <#bulk_output-1>`__   | Output a bulked message to a log-file.                                        |
+---------------------------------------+-------------------------------------------------------------------------------+
| `close/1 <#close-1>`__                | Close a logger.                                                               |
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
| `rotate/1 <#rotate-1>`__              | Rotate a log-file.                                                            |
+---------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/4 <#start_link-4>`__     | Start the server.                                                             |
+---------------------------------------+-------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                  | Stop the server.                                                              |
+---------------------------------------+-------------------------------------------------------------------------------+
| `sync/1 <#sync-1>`__                  | Synchronize a message to a log-file.                                          |
+---------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__        | This function is called by a gen\_server when it is about to terminate.       |
+---------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

append/3
~~~~~~~~

``append(Method, Id, Log) -> ok``

-  ``Method = '?LOG_APPEND_SYNC' | '?LOG_APPEND_ASYNC'``
-  ``Id = atom()``
-  ``Log = any()``

Append a message to a log-file.

append/4
~~~~~~~~

``append(X1, Id, Log, Level) -> any()``

bulk\_output/1
~~~~~~~~~~~~~~

``bulk_output(Id) -> ok``

-  ``Id = atom()``

Output a bulked message to a log-file.

close/1
~~~~~~~

``close(Id) -> ok``

-  ``Id = atom()``

Close a logger

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

``handle_cast(X1, Logger_state) -> any()``

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

rotate/1
~~~~~~~~

``rotate(Id) -> ok``

-  ``Id = atom()``

Rotate a log-file.

start\_link/4
~~~~~~~~~~~~~

``start_link(Id, Appender, CallbackMod, Props) -> {ok, pid()} | ignore | {error, any()}``

-  ``Id = atom()``
-  ``Appender = atom()``
-  ``CallbackMod = module()``
-  ``Props = [{atom(), any()}]``

Start the server

stop/1
~~~~~~

``stop(Id) -> ok``

-  ``Id = pid() | atom()``

Stop the server

sync/1
~~~~~~

``sync(Id) -> ok``

-  ``Id = atom()``

Synchronize a message to a log-file.

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason.
