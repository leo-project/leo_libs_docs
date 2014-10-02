leo\_metrics\_req\_notifier
==================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The notifier of request metrics.

**Behaviours:**
```svc_notify_behaviour`` <svc_notify_behaviour.html>`__.

**References**

-  ```https://github.com/leo-project/leo_statistics/blob/master/src/leo_metrics_req_notifier.erl`` <https://github.com/leo-project/leo_statistics/blob/master/src/leo_metrics_req_notifier.erl>`__

Description
-----------

The notifier of request metrics

Function Index
--------------

+----------------------------+-----------------------+
| `notify/1 <#notify-1>`__   | Notify the message.   |
+----------------------------+-----------------------+

Function Details
----------------

notify/1
~~~~~~~~

``notify(Msg) -> ok | {error, any()}``

-  ``Msg = #sv_result{}``

Notify the message
