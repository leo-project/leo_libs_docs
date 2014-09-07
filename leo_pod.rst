leo\_pod
===============

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

API of leo\_pod.

**References**

-  https://github.com/leo-project/leo\_pod/blob/master/src/leo\_pod.erl

Description
-----------

API of leo\_pod

Function Index
--------------

+-------------------------------------------+------------------------------------------------------------+
| `checkin/2 <#checkin-2>`__                | Checkin the worker into the worker pool.                   |
+-------------------------------------------+------------------------------------------------------------+
| `checkin\_async/2 <#checkin_async-2>`__   | Checkin the worker into the worker pool assynchronously.   |
+-------------------------------------------+------------------------------------------------------------+
| `checkout/1 <#checkout-1>`__              | Checkout a worker from the worker pool.                    |
+-------------------------------------------+------------------------------------------------------------+
| `start\_link/6 <#start_link-6>`__         | Initialize a work pool.                                    |
+-------------------------------------------+------------------------------------------------------------+
| `status/1 <#status-1>`__                  | Get the status of the worker pool.                         |
+-------------------------------------------+------------------------------------------------------------+
| `stop/1 <#stop-1>`__                      | Stop the worker pool.                                      |
+-------------------------------------------+------------------------------------------------------------+

Function Details
----------------

checkin/2
~~~~~~~~~

``checkin(PodName, Worker) -> ok``

-  ``PodName = atom()``
-  ``Worker = pid()``

Checkin the worker into the worker pool.

checkin\_async/2
~~~~~~~~~~~~~~~~

``checkin_async(PodName, Worker) -> ok``

-  ``PodName = atom()``
-  ``Worker = pid()``

Checkin the worker into the worker pool assynchronously.

checkout/1
~~~~~~~~~~

``checkout(PodName) -> {ok, pid()}``

-  ``PodName = atom()``

Checkout a worker from the worker pool.

start\_link/6
~~~~~~~~~~~~~

``start_link(PodName, PodSize, MaxOverflow, WorkerMod, WorkerArgs, InitFun) -> {ok, pid()}``

-  ``PodName = atom()``
-  ``PodSize = non_neg_integer()``
-  ``MaxOverflow = non_neg_integer()``
-  ``WorkerMod = module()``
-  ``WorkerArgs = [any()]``
-  ``InitFun = function()``

Initialize a work pool.

status/1
~~~~~~~~

``status(PodName) -> {ok, {NumOfWorking, NumOfWating, NumOfRoomForOverflow}}``

-  ``PodName = atom()``
-  ``NumOfWorking = non_neg_integer()``
-  ``NumOfWating = non_neg_integer()``
-  ``NumOfRoomForOverflow = non_neg_integer()``

Get the status of the worker pool. It returns the tuple of the numbers
of working\_processes, waiting processes, and room of overflow.

stop/1
~~~~~~

``stop(PodName) -> true | not_started``

-  ``PodName = atom()``

Stop the worker pool.
