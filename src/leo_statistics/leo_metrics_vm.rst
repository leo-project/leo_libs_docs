leo\_metrics\_vm
=======================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The metrics of Erlang VM's statistics.

**Behaviours:**
```leo_statistics_behaviour`` <leo_statistics_behaviour.html>`__.

**References**

-  ```https://github.com/leo-project/leo_statistics/blob/master/src/leo_metrics_vm.erl`` <https://github.com/leo-project/leo_statistics/blob/master/src/leo_metrics_vm.erl>`__

Description
-----------

The metrics of Erlang VM's statistics

Function Index
--------------

+-------------------------------------------+----------------------+
| `handle\_notify/0 <#handle_notify-0>`__   |                      |
+-------------------------------------------+----------------------+
| `start\_link/1 <#start_link-1>`__         | Start the metrics.   |
+-------------------------------------------+----------------------+

Function Details
----------------

handle\_notify/0
~~~~~~~~~~~~~~~~

| ``handle_notify() -> ok``

start\_link/1
~~~~~~~~~~~~~

``start_link(Window) -> ok | {error, any()}``

-  ``Window = non_neg_integer()``

Start the metrics
