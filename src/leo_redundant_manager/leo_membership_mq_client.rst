leo\_membership\_mq\_client
==================================

-  `Description <#description>`__
-  `Data Types <#types>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The membership operation's messsage-queues client.

**Behaviours:** ```leo_mq_behaviour`` <leo_mq_behaviour.html>`__.

**References**

-  ```https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_membership_mq_client.erl`` <https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_membership_mq_client.erl>`__

Description
-----------

The membership operation's messsage-queues client

Data Types
----------

type\_of\_server()
~~~~~~~~~~~~~~~~~~

``type_of_server() = manager | gateway | storage``

Function Index
--------------

+---------------------------------------+----------------------------------------+
| `handle\_call/1 <#handle_call-1>`__   | Publish callback function.             |
+---------------------------------------+----------------------------------------+
| `handle\_call/3 <#handle_call-3>`__   |                                        |
+---------------------------------------+----------------------------------------+
| `init/0 <#init-0>`__                  | Initializer.                           |
+---------------------------------------+----------------------------------------+
| `publish/3 <#publish-3>`__            | Publish a message into the queue.      |
+---------------------------------------+----------------------------------------+
| `start/2 <#start-2>`__                | create queues and launch mq-servers.   |
+---------------------------------------+----------------------------------------+

Function Details
----------------

handle\_call/1
~~~~~~~~~~~~~~

``handle_call(X1::{publish | consume, Id, Reply}) -> ok``

-  ``Id = any()``
-  ``Reply = any()``

Publish callback function

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(X1, X2, X3) -> any()``

init/0
~~~~~~

| ``init() -> ok``

Initializer

publish/3
~~~~~~~~~

``publish(ServerType, Node, Error) -> ok | {error, any()}``

-  ``ServerType = atom()``
-  ``Node = atom()``
-  ``Error = any()``

Publish a message into the queue.

start/2
~~~~~~~

``start(ServerType, RootPath) -> ok | {error, any()}``

-  ``ServerType = type_of_server()``
-  ``RootPath = string()``

create queues and launch mq-servers.
