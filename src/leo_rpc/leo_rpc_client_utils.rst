leo\_rpc\_client\_utils
==============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_rpc\_client\_utils is a utility module.

**References**

-  https://github.com/leo-project/leo\_rpc/blob/master/src/leo\_rpc\_client\_utils

Description
-----------

leo\_rpc\_client\_utils is a utility module

Function Index
--------------

+-----------------------------------------------------------------+-------------------------------------------------+
| `create\_client\_worker\_id/2 <#create_client_worker_id-2>`__   | Generate client-worker-id from host and port.   |
+-----------------------------------------------------------------+-------------------------------------------------+
| `get\_client\_worker\_id/2 <#get_client_worker_id-2>`__         | Retrieve client-worker's id by host and port.   |
+-----------------------------------------------------------------+-------------------------------------------------+

Function Details
----------------

create\_client\_worker\_id/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``create_client_worker_id(Host, Port) -> string()``

-  ``Host = string()``
-  ``Port = pos_integer()``

Generate client-worker-id from host and port

get\_client\_worker\_id/2
~~~~~~~~~~~~~~~~~~~~~~~~~

``get_client_worker_id(Host, Port) -> atom()``

-  ``Host = string() | atom()``
-  ``Port = pos_integer()``

Retrieve client-worker's id by host and port
