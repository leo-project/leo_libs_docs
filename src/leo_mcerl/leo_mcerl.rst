leo\_mcerl
=================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The mcerl API.

**References**

-  https://github.com/leo-project/leo\_mcerl/blob/master/src/leo\_mcerl.erl

Description
-----------

The mcerl API

Function Index
--------------

+----------------------------+-------------------------------------------+
| `delete/2 <#delete-2>`__   | Delete an object from the leo\_mcerl.     |
+----------------------------+-------------------------------------------+
| `get/2 <#get-2>`__         | Retrieve an object from the leo\_mcerl.   |
+----------------------------+-------------------------------------------+
| `items/1 <#items-1>`__     | Retrieve total of cached objects.         |
+----------------------------+-------------------------------------------+
| `put/3 <#put-3>`__         | Insert an object into the leo\_mcerl.     |
+----------------------------+-------------------------------------------+
| `size/1 <#size-1>`__       | Retrieve size of cached objects.          |
+----------------------------+-------------------------------------------+
| `start/1 <#start-1>`__     | Launch leo\_mcerl.                        |
+----------------------------+-------------------------------------------+
| `stop/1 <#stop-1>`__       | Halt the leo\_mcerl.                      |
+----------------------------+-------------------------------------------+

Function Details
----------------

delete/2
~~~~~~~~

``delete(Res, Key) -> ok | {error, any()}``

-  ``Res = any()``
-  ``Key = binary()``

Delete an object from the leo\_mcerl

get/2
~~~~~

``get(Res, Key) -> {ok, binary()} | not_found | {error, any()}``

-  ``Res = any()``
-  ``Key = binary()``

Retrieve an object from the leo\_mcerl

items/1
~~~~~~~

``items(Res) -> {ok, integer()} | {error, any()}``

-  ``Res = any()``

Retrieve total of cached objects

put/3
~~~~~

``put(Res, Key, Value) -> ok | {error, any()}``

-  ``Res = any()``
-  ``Key = binary()``
-  ``Value = binary()``

Insert an object into the leo\_mcerl

size/1
~~~~~~

``size(Res) -> {ok, integer()} | {error, any()}``

-  ``Res = any()``

Retrieve size of cached objects

start/1
~~~~~~~

``start(Size) -> {ok, any()}``

-  ``Size = integer()``

Launch leo\_mcerl

stop/1
~~~~~~

``stop(Res) -> ok | {error, any()}``

-  ``Res = any()``

Halt the leo\_mcerl
