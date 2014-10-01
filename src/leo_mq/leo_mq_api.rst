leo\_mq\_api
===================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_mq's API.

**References**

-  ```https://github.com/leo-project/leo_mq/blob/master/src/leo_mq_api.erl`` <https://github.com/leo-project/leo_mq/blob/master/src/leo_mq_api.erl>`__

Description
-----------

leo\_mq's API

Function Index
--------------

+------------------------------+--------------------------------------------+
| `new/2 <#new-2>`__           | Create a new message-queue server.         |
+------------------------------+--------------------------------------------+
| `new/3 <#new-3>`__           |                                            |
+------------------------------+--------------------------------------------+
| `publish/3 <#publish-3>`__   | Publish a message into the queue.          |
+------------------------------+--------------------------------------------+
| `status/1 <#status-1>`__     | Retrieve a current state from the queue.   |
+------------------------------+--------------------------------------------+

Function Details
----------------

new/2
~~~~~

``new(Id, Properties) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Properties = [atom()] | #mq_properties{}``

Create a new message-queue server

new/3
~~~~~

``new(RefSup, Id, Properties) -> ok | {error, any()}``

-  ``RefSup = atom() | pid()``
-  ``Id = atom()``
-  ``Properties = [atom()] | #mq_properties{}``

publish/3
~~~~~~~~~

``publish(Id, KeyBin, MessageBin) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``KeyBin = binary()``
-  ``MessageBin = binary()``

Publish a message into the queue

status/1
~~~~~~~~

``status(Id) -> {ok, list()}``

-  ``Id = atom()``

Retrieve a current state from the queue
