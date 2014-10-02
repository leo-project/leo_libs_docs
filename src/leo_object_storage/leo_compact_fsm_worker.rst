leo\_compact\_fsm\_worker
================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

FSM of the data-compaction worker, which handles removing unnecessary
objects from a object container.

**Behaviours:** ```gen_fsm`` <gen_fsm.html>`__.

**References**

-  https://github.com/leo-project/leo\_object\_storage/blob/master/src/leo\_compact\_fsm\_controller.erl

Description
-----------

FSM of the data-compaction worker, which handles removing unnecessary
objects from a object container.

Function Index
--------------

+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `code\_change/4 <#code_change-4>`__                | Convert process state when code is changed.                                                                               |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `finish/1 <#finish-1>`__                           | Remove an object from the object-storage - (logical-delete).                                                              |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `format\_status/2 <#format_status-2>`__            | This function is called by a gen\_fsm when it should update its internal state data during a release upgrade/downgrade.   |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `handle\_event/3 <#handle_event-3>`__              | Handle events.                                                                                                            |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `handle\_info/3 <#handle_info-3>`__                | Handling all non call/cast messages.                                                                                      |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `handle\_sync\_event/4 <#handle_sync_event-4>`__   | Handle 'status' event.                                                                                                    |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `idling/2 <#idling-2>`__                           |                                                                                                                           |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `idling/3 <#idling-3>`__                           | State of 'idle'.                                                                                                          |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                               | Initiates the server.                                                                                                     |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `resume/1 <#resume-1>`__                           | Remove an object from the object-storage - (logical-delete).                                                              |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `run/2 <#run-2>`__                                 | Run the process.                                                                                                          |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `run/4 <#run-4>`__                                 |                                                                                                                           |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `running/2 <#running-2>`__                         | State of 'running'.                                                                                                       |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `running/3 <#running-3>`__                         |                                                                                                                           |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `start\_link/4 <#start_link-4>`__                  | Creates a gen\_fsm process as part of a supervision tree.                                                                 |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `state/2 <#state-2>`__                             | Retrieve the storage stats specfied by Id which contains number of objects and so on.                                     |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                               | Stop this server.                                                                                                         |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `suspend/1 <#suspend-1>`__                         | Retrieve an object from the object-storage.                                                                               |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `suspending/2 <#suspending-2>`__                   | State of 'suspend'.                                                                                                       |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `suspending/3 <#suspending-3>`__                   |                                                                                                                           |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `terminate/3 <#terminate-3>`__                     | This function is called by a gen\_server when it is about to terminate.                                                   |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+

Function Details
----------------

code\_change/4
~~~~~~~~~~~~~~

``code_change(OldVsn, StateName, State, Extra) -> any()``

Convert process state when code is changed

finish/1
~~~~~~~~

``finish(Id) -> ok | {error, any()}``

-  ``Id = atom()``

Remove an object from the object-storage - (logical-delete)

format\_status/2
~~~~~~~~~~~~~~~~

``format_status(Opt, X2) -> any()``

This function is called by a gen\_fsm when it should update its internal
state data during a release upgrade/downgrade

handle\_event/3
~~~~~~~~~~~~~~~

``handle_event(Event, StateName, State) -> any()``

Handle events

handle\_info/3
~~~~~~~~~~~~~~

``handle_info(Info, StateName, State) -> any()``

Handling all non call/cast messages

handle\_sync\_event/4
~~~~~~~~~~~~~~~~~~~~~

``handle_sync_event(X1, From, StateName, State) -> any()``

Handle 'status' event

idling/2
~~~~~~~~

``idling(EventInfo, State) -> {next_state, '?ST_IDLING', State}``

-  ``EventInfo = #event_info{}``
-  ``State = #state{}``

idling/3
~~~~~~~~

``idling(EventInfo, From, State) -> {next_state, '?ST_IDLING' | '?ST_RUNNING', State}``

-  ``EventInfo = #event_info{}``
-  ``From = {pid(), Tag::atom()}``
-  ``State = #state{}``

State of 'idle'

init/1
~~~~~~

``init(X1) -> any()``

Initiates the server

resume/1
~~~~~~~~

``resume(Id) -> ok | {error, any()}``

-  ``Id = atom()``

Remove an object from the object-storage - (logical-delete)

run/2
~~~~~

``run(Id, IsDiagnose) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``IsDiagnose = boolean()``

Run the process

run/4
~~~~~

``run(Id, ControllerPid, IsDiagnose, CallbackFun) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``ControllerPid = pid()``
-  ``IsDiagnose = boolean()``
-  ``CallbackFun = function()``

running/2
~~~~~~~~~

``running(EventInfo, State) -> {next_state, '?ST_RUNNING', State}``

-  ``EventInfo = #event_info{}``
-  ``State = #state{}``

State of 'running'

running/3
~~~~~~~~~

| ``running(X1::term(), From::term(), State::#state{}) -> {next_state, '?ST_SUSPENDING' | '?ST_RUNNING', #state{}}``

start\_link/4
~~~~~~~~~~~~~

``start_link(Id, ObjStorageId, MetaDBId, LoggerId) -> {ok, pid()} | {error, any()}``

-  ``Id = atom()``
-  ``ObjStorageId = atom()``
-  ``MetaDBId = atom()``
-  ``LoggerId = atom()``

Creates a gen\_fsm process as part of a supervision tree

state/2
~~~~~~~

``state(Id, Client) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Client = pid()``

Retrieve the storage stats specfied by Id which contains number of
objects and so on.

stop/1
~~~~~~

``stop(Id) -> ok``

-  ``Id = atom()``

Stop this server

suspend/1
~~~~~~~~~

``suspend(Id) -> ok | {error, any()}``

-  ``Id = atom()``

Retrieve an object from the object-storage

suspending/2
~~~~~~~~~~~~

``suspending(EventInfo, State) -> {next_state, '?ST_SUSPENDING', State}``

-  ``EventInfo = #event_info{}``
-  ``State = #state{}``

State of 'suspend'

suspending/3
~~~~~~~~~~~~

``suspending(EventInfo, From, State) -> {next_state, '?ST_SUSPENDING' | '?ST_RUNNING', State}``

-  ``EventInfo = #event_info{}``
-  ``From = {pid(), Tag::atom()}``
-  ``State = #state{}``

terminate/3
~~~~~~~~~~~

``terminate(Reason, StateName, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason. The return
value is ignored.
