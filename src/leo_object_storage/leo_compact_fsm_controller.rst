leo\_compact\_fsm\_controller
====================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

FSM of the data-compaction controller, which manages FSM of the
data-compaction's workers.

**Behaviours:** ```gen_fsm`` <gen_fsm.html>`__.

**References**

-  https://github.com/leo-project/leo\_object\_storage/blob/master/src/leo\_compact\_fsm\_controller.erl

Description
-----------

FSM of the data-compaction controller, which manages FSM of the
data-compaction's workers

Function Index
--------------

+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `code\_change/4 <#code_change-4>`__                | Convert process state when code is changed.                                                                               |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `diagnose/0 <#diagnose-0>`__                       | Request diagnosing data-compaction to the data-compaction's workers.                                                      |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `finish/3 <#finish-3>`__                           | Terminate a child.                                                                                                        |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `format\_status/2 <#format_status-2>`__            | This function is called by a gen\_fsm when it should update its internal state data during a release upgrade/downgrade.   |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `handle\_event/3 <#handle_event-3>`__              | Handle events.                                                                                                            |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `handle\_info/3 <#handle_info-3>`__                | Handling all non call/cast messages.                                                                                      |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `handle\_sync\_event/4 <#handle_sync_event-4>`__   | Handle 'state' event.                                                                                                     |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `idling/2 <#idling-2>`__                           | State of 'idle'.                                                                                                          |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `idling/3 <#idling-3>`__                           | State of 'idle'.                                                                                                          |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                               | Initiates the server.                                                                                                     |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `lock/1 <#lock-1>`__                               | Request 'lock'.                                                                                                           |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `resume/0 <#resume-0>`__                           | Request 'resume compaction' to the data-compaction's workers.                                                             |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `run/0 <#run-0>`__                                 | Request launch of data-compaction to the data-compaction's workers.                                                       |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `run/1 <#run-1>`__                                 |                                                                                                                           |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `run/2 <#run-2>`__                                 |                                                                                                                           |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `run/3 <#run-3>`__                                 |                                                                                                                           |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `running/2 <#running-2>`__                         | State of 'running'.                                                                                                       |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `running/3 <#running-3>`__                         | State of 'running'.                                                                                                       |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `start\_link/0 <#start_link-0>`__                  | Creates a gen\_fsm process as part of a supervision tree.                                                                 |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `state/0 <#state-0>`__                             | Retrieve the all compaction statuses from the data-compaction's workers.                                                  |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                               | Request stop of data-compaction to the data-compaction's workers.                                                         |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `suspend/0 <#suspend-0>`__                         | Request 'suspend compaction' to the data-compaction's workers.                                                            |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `suspending/2 <#suspending-2>`__                   | State of 'suspend'.                                                                                                       |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `suspending/3 <#suspending-3>`__                   | State of 'suspend'.                                                                                                       |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+
| `terminate/3 <#terminate-3>`__                     | This function is called by a gen\_server when it is about to terminate.                                                   |
+----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------+

Function Details
----------------

code\_change/4
~~~~~~~~~~~~~~

``code_change(OldVsn, StateName, State, Extra) -> any()``

Convert process state when code is changed

diagnose/0
~~~~~~~~~~

| ``diagnose() -> term()``

Request diagnosing data-compaction to the data-compaction's workers

finish/3
~~~~~~~~

``finish(Pid, FinishedId, AccErrors) -> term()``

-  ``Pid = pid()``
-  ``FinishedId = atom()``
-  ``AccErrors = [{pos_integer(), pos_integer()}]``

Terminate a child

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

Handle 'state' event

idling/2
~~~~~~~~

``idling(EventInfo, State) -> {stop, string(), State}``

-  ``EventInfo = #event_info{}``
-  ``State = #state{}``

State of 'idle'

idling/3
~~~~~~~~

``idling(EventInfo, From, State) -> {next_state, '?ST_RUNNING' | '?ST_IDLING', State}``

-  ``EventInfo = #event_info{} | any()``
-  ``From = {pid(), Tag::atom()}``
-  ``State = #state{}``

State of 'idle'

init/1
~~~~~~

``init(Option) -> {ok, '?ST_IDLING', State}``

-  ``Option = [any()]``
-  ``State = #state{}``

Initiates the server

lock/1
~~~~~~

``lock(Id) -> term()``

-  ``Id = atom()``

Request 'lock'

resume/0
~~~~~~~~

| ``resume() -> term()``

Request 'resume compaction' to the data-compaction's workers

run/0
~~~~~

| ``run() -> term()``

Request launch of data-compaction to the data-compaction's workers

run/1
~~~~~

``run(MaxConn) -> term()``

-  ``MaxConn = pos_integer()``

run/2
~~~~~

``run(MaxConn, CallbackFun) -> term()``

-  ``MaxConn = pos_integer()``
-  ``CallbackFun = function()``

run/3
~~~~~

``run(TargetPids, MaxConn, CallbackFun) -> term()``

-  ``TargetPids = [pid() | atom()]``
-  ``MaxConn = pos_integer()``
-  ``CallbackFun = function()``

running/2
~~~~~~~~~

``running(EventInfo, State) -> {next_state, running, State}``

-  ``EventInfo = #event_info{}``
-  ``State = #state{}``

State of 'running'

running/3
~~~~~~~~~

``running(EventInfo, From, State) -> {next_state, '?ST_RUNNING' | '?ST_SUSPENDING', State}``

-  ``EventInfo = #event_info{} | '?EVENT_SUSPEND' | any()``
-  ``From = {pid(), Tag::atom()}``
-  ``State = #state{}``

State of 'running'

start\_link/0
~~~~~~~~~~~~~

| ``start_link() -> {ok, pid()} | ignore | {error, any()}``

Creates a gen\_fsm process as part of a supervision tree

state/0
~~~~~~~

| ``state() -> term()``

Retrieve the all compaction statuses from the data-compaction's workers

stop/1
~~~~~~

``stop(Id) -> term()``

-  ``Id = atom()``

Request stop of data-compaction to the data-compaction's workers

suspend/0
~~~~~~~~~

| ``suspend() -> term()``

Request 'suspend compaction' to the data-compaction's workers

suspending/2
~~~~~~~~~~~~

``suspending(EventInfo, State) -> {next_state, '?ST_SUSPENDING' | '?ST_IDLING', State}``

-  ``EventInfo = #event_info{}``
-  ``State = #state{}``

State of 'suspend'

suspending/3
~~~~~~~~~~~~

``suspending(EventInfo, From, State) -> {next_state, '?ST_SUSPENDING' | '?ST_RUNNING', State}``

-  ``EventInfo = #event_info{}``
-  ``From = {pid(), Tag::atom()}``
-  ``State = #state{}``

State of 'suspend'

terminate/3
~~~~~~~~~~~

``terminate(Reason, StateName, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason. The return
value is ignored.
