leo\_metrics\_req
========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The metrics of request.

**Behaviours:**
```leo_statistics_behaviour`` <leo_statistics_behaviour.html>`__.

**References**

-  ```https://github.com/leo-project/leo_statistics/blob/master/src/leo_metrics_req.erl`` <https://github.com/leo-project/leo_statistics/blob/master/src/leo_metrics_req.erl>`__

Description
-----------

The metrics of request

Function Index
--------------

+-------------------------------------------+-----------------------------------------------------+
| `handle\_notify/0 <#handle_notify-0>`__   |                                                     |
+-------------------------------------------+-----------------------------------------------------+
| `notify/1 <#notify-1>`__                  | Put a value into the savanna from an application.   |
+-------------------------------------------+-----------------------------------------------------+
| `notify/2 <#notify-2>`__                  |                                                     |
+-------------------------------------------+-----------------------------------------------------+
| `start\_link/1 <#start_link-1>`__         | Start the metrics.                                  |
+-------------------------------------------+-----------------------------------------------------+

Function Details
----------------

handle\_notify/0
~~~~~~~~~~~~~~~~

| ``handle_notify() -> ok``

notify/1
~~~~~~~~

``notify(Column) -> ok | {error, any()}``

-  ``Column = atom()``

Put a value into the savanna from an application

notify/2
~~~~~~~~

``notify(Key, Size) -> ok | {error, any()}``

-  ``Key = atom()``
-  ``Size = pos_integer()``

start\_link/1
~~~~~~~~~~~~~

``start_link(Window) -> ok | {error, any()}``

-  ``Window = non_neg_integer()``

Start the metrics
