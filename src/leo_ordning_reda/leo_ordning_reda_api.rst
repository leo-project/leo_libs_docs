leo\_ordning\_reda\_api
==============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The ordning-reda's API.

**References**

-  https://github.com/leo-project/leo\_ordning\_reda/blob/master/src/leo\_ordning\_reda\_api.erl

Description
-----------

The ordning-reda's API

Function Index
--------------

+-------------------------------------------------+----------------------------------------+
| `add\_container/2 <#add_container-2>`__         | Add the container into the App.        |
+-------------------------------------------------+----------------------------------------+
| `has\_container/1 <#has_container-1>`__         | Check whether the container exists.    |
+-------------------------------------------------+----------------------------------------+
| `pack/1 <#pack-1>`__                            | Pack the object.                       |
+-------------------------------------------------+----------------------------------------+
| `remove\_container/1 <#remove_container-1>`__   | Remove the container from the App.     |
+-------------------------------------------------+----------------------------------------+
| `stack/3 <#stack-3>`__                          | Stack the object into the container.   |
+-------------------------------------------------+----------------------------------------+
| `start/0 <#start-0>`__                          | Launch the application.                |
+-------------------------------------------------+----------------------------------------+
| `stop/0 <#stop-0>`__                            | Stop the application.                  |
+-------------------------------------------------+----------------------------------------+
| `unpack/2 <#unpack-2>`__                        | Unpack the object.                     |
+-------------------------------------------------+----------------------------------------+

Function Details
----------------

add\_container/2
~~~~~~~~~~~~~~~~

``add_container(Unit, Options) -> ok | {error, any()}``

-  ``Unit = atom()``
-  ``Options = [any()]``

Add the container into the App

has\_container/1
~~~~~~~~~~~~~~~~

``has_container(Unit) -> true | false``

-  ``Unit = atom()``

Check whether the container exists

pack/1
~~~~~~

``pack(Object) -> {ok, Bin} | {error, term()}``

-  ``Object = any()``
-  ``Bin = binary()``

Pack the object

remove\_container/1
~~~~~~~~~~~~~~~~~~~

``remove_container(Unit) -> ok | {error, any()}``

-  ``Unit = atom()``

Remove the container from the App

stack/3
~~~~~~~

``stack(Unit, StrawId, Object) -> ok | {error, any()}``

-  ``Unit = atom()``
-  ``StrawId = any()``
-  ``Object = binary()``

Stack the object into the container

start/0
~~~~~~~

| ``start() -> ok | {error, any()}``

Launch the application

stop/0
~~~~~~

| ``stop() -> ok | {error, any()}``

Stop the application

unpack/2
~~~~~~~~

``unpack(CompressedBin, Fun) -> ok``

-  ``CompressedBin = binary()``
-  ``Fun = function()``

Unpack the object
