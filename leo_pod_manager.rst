leo\_pod\_manager
========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_pod\_manager can manage worker pools in the pod.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  https://github.com/leo-project/leo\_pod/blob/master/src/leo\_pod\_manager.erl

Description
-----------

leo\_pod\_manager can manage worker pools in the pod

Function Index
--------------

+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `checkin/2 <#checkin-2>`__                | Check in a worker to the woker pool.                                                                                                     |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `checkin\_async/2 <#checkin_async-2>`__   | Check in a worker to the worker pool with asynchronous.                                                                                  |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `checkout/1 <#checkout-1>`__              | Check out a worker from the worker pool.                                                                                                 |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `close/1 <#close-1>`__                    | Retrieve pids of specified PodName.                                                                                                      |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__       | gen\_server callback - Module:code\_change(OldVsn, State, Extra) -> {ok, NewState} \| {error, Reason}.                                   |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__       | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.                                                              |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__       | gen\_server callback - Module:handle\_cast(Request, State) -> Result.                                                                    |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__       | gen\_server callback - Module:handle\_info(Info, State) -> Result.                                                                       |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                      | gen\_server callback - Module:init(Args) -> Result.                                                                                      |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `pool\_pids/1 <#pool_pids-1>`__           | Retrieve pids of specified PodName.                                                                                                      |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `raw\_status/1 <#raw_status-1>`__         | Retrieve a raw status of specified PodName.                                                                                              |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `start\_link/6 <#start_link-6>`__         | Initialize a wooker pool.                                                                                                                |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `status/1 <#status-1>`__                  | Retrieve the current status in pretty format as follows: format: { working\_process\_count, worker\_process\_count, overflow\_count }.   |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                      | Stop the worker pool.                                                                                                                    |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__            | gen\_server callback - Module:terminate(Reason, State).                                                                                  |
+-------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+

Function Details
----------------

checkin/2
~~~~~~~~~

``checkin(PodName, WorkerPid) -> ok | {error, any()}``

-  ``PodName = atom()``
-  ``WorkerPid = pid()``

Check in a worker to the woker pool

checkin\_async/2
~~~~~~~~~~~~~~~~

``checkin_async(PodName, WorkerPid) -> ok``

-  ``PodName = atom()``
-  ``WorkerPid = pid()``

Check in a worker to the worker pool with asynchronous

checkout/1
~~~~~~~~~~

``checkout(PodName) -> {ok, pid()} | {error, empty}``

-  ``PodName = atom()``

Check out a worker from the worker pool

close/1
~~~~~~~

``close(PodName) -> ok | {error, any()}``

-  ``PodName = atom()``

Retrieve pids of specified PodName

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

gen\_server callback - Module:code\_change(OldVsn, State, Extra) -> {ok,
NewState} \| {error, Reason}

Description: Convert process state when code is changed

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(X1, From, State) -> any()``

gen\_server callback - Module:handle\_call(Request, From, State) ->
Result

handle\_cast/2
~~~~~~~~~~~~~~

``handle_cast(X1, State) -> any()``

gen\_server callback - Module:handle\_cast(Request, State) -> Result

handle\_info/2
~~~~~~~~~~~~~~

``handle_info(Info, State) -> any()``

gen\_server callback - Module:handle\_info(Info, State) -> Result

init/1
~~~~~~

``init(X1) -> any()``

gen\_server callback - Module:init(Args) -> Result

pool\_pids/1
~~~~~~~~~~~~

``pool_pids(PodName) -> {ok, [pid()]} | {error, any()}``

-  ``PodName = atom()``

Retrieve pids of specified PodName

raw\_status/1
~~~~~~~~~~~~~

``raw_status(PodName) -> {ok, [tuple()]} | {error, any()}``

-  ``PodName = atom()``

Retrieve a raw status of specified PodName

start\_link/6
~~~~~~~~~~~~~

``start_link(PodName, NumOfChildren, MaxOverflow, WorkerMod, WorkerArgs, InitFun) -> {ok, pid()} | ignore | {error, any()}``

-  ``PodName = atom()``
-  ``NumOfChildren = pos_integer()``
-  ``MaxOverflow = non_neg_integer()``
-  ``WorkerMod = module()``
-  ``WorkerArgs = [any()]``
-  ``InitFun = function()``

Initialize a wooker pool

status/1
~~~~~~~~

``status(PodName) -> {ok, {NumOfWorking, NumOfWating, NumOfRoomForOverflow}}``

-  ``PodName = atom()``
-  ``NumOfWorking = non_neg_integer()``
-  ``NumOfWating = non_neg_integer()``
-  ``NumOfRoomForOverflow = non_neg_integer()``

Retrieve the current status in pretty format as follows: format: {
working\_process\_count, worker\_process\_count, overflow\_count }

stop/1
~~~~~~

``stop(PodName) -> ok | {error, any()}``

-  ``PodName = atom()``

Stop the worker pool

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

gen\_server callback - Module:terminate(Reason, State)

Description: This function is called by a gen\_server when it is about
to terminate. It should be the opposite of Module:init/1 and do any
necessary cleaning up. When it returns, the gen\_server terminates with
Reason. The return value is ignored.
