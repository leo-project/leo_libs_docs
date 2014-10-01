leo\_mq\_server
======================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The gen\_server process for the process of a mq as part of a supervision
tree.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  ```https://github.com/leo-project/leo_mq/blob/master/src/leo_mq_server.erl`` <https://github.com/leo-project/leo_mq/blob/master/src/leo_mq_server.erl>`__

Description
-----------

The gen\_server process for the process of a mq as part of a supervision
tree

Function Index
--------------

+---------------------------------------+-------------------------------------------------------------------------------+
| `close/1 <#close-1>`__                | get state from the queue.                                                     |
+---------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__   | Convert process state when code is changed.                                   |
+---------------------------------------+-------------------------------------------------------------------------------+
| `consume/1 <#consume-1>`__            | Consume a message from the queue.                                             |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__   | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.   |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__   | gen\_server callback - Module:handle\_cast(Request, State) -> Result.         |
+---------------------------------------+-------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__   | gen\_server callback - Module:handle\_info(Info, State) -> Result.            |
+---------------------------------------+-------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                  | gen\_server callback - Module:init(Args) -> Result.                           |
+---------------------------------------+-------------------------------------------------------------------------------+
| `publish/3 <#publish-3>`__            | Register a queuing data.                                                      |
+---------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/2 <#start_link-2>`__     | Creates the gen\_server process as part of a supervision tree.                |
+---------------------------------------+-------------------------------------------------------------------------------+
| `status/1 <#status-1>`__              | Retrieve the current state from the queue.                                    |
+---------------------------------------+-------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                  | Close the process.                                                            |
+---------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__        | This function is called by a gen\_server when it is about to terminate.       |
+---------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

close/1
~~~~~~~

``close(Id) -> ok``

-  ``Id = atom()``

get state from the queue.

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

gen\_server callback - Module:code\_change(OldVsn, State, Extra) -> {ok,
NewState} \| {error, Reason}.

consume/1
~~~~~~~~~

``consume(Id) -> ok | {error, any()}``

-  ``Id = atom()``

Consume a message from the queue.

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(X1, From, State) -> any()``

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

publish/3
~~~~~~~~~

``publish(Id, KeyBin, MessageBin) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``KeyBin = binary()``
-  ``MessageBin = binary()``

Register a queuing data.

start\_link/2
~~~~~~~~~~~~~

``start_link(Id, Props) -> {ok, pid()} | ignore | {error, any()}``

-  ``Id = atom()``
-  ``Props = [tuple()]``

Creates the gen\_server process as part of a supervision tree

status/1
~~~~~~~~

``status(Id) -> {ok, list()}``

-  ``Id = atom()``

Retrieve the current state from the queue.

stop/1
~~~~~~

``stop(Id) -> ok | {error, any()}``

-  ``Id = atom()``

Close the process

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason. The return
value is ignored.

gen\_server callback - Module:terminate(Reason, State)
