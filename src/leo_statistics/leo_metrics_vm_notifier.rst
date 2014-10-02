leo\_metrics\_vm\_notifier
=================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The notifier of Erlang VM's metrics.

**Behaviours:**
```svc_notify_behaviour`` <svc_notify_behaviour.html>`__.

**References**

-  ```https://github.com/leo-project/leo_statistics/blob/master/src/leo_statistics_sampler.erl`` <https://github.com/leo-project/leo_statistics/blob/master/src/leo_statistics_sampler.erl>`__

Description
-----------

The notifier of Erlang VM's metrics

Function Index
--------------

+----------------------------+----+
| `notify/1 <#notify-1>`__   |    |
+----------------------------+----+

Function Details
----------------

notify/1
~~~~~~~~

``notify(Msg) -> ok | {error, any()}``

-  ``Msg = #sv_result{}``
