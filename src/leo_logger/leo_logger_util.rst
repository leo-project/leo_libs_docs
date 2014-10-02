leo\_logger\_util
========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The log utils.

**References**

-  https://github.com/leo-project/leo\_logger/blob/master/src/leo\_logger\_util.erl

Description
-----------

The log utils

Function Index
--------------

+-----------------------------------------+---------------------------------+
| `add\_appender/2 <#add_appender-2>`__   | add an appender into the ets.   |
+-----------------------------------------+---------------------------------+
| `new/3 <#new-3>`__                      | create a logger proc.           |
+-----------------------------------------+---------------------------------+
| `new/4 <#new-4>`__                      |                                 |
+-----------------------------------------+---------------------------------+
| `new/5 <#new-5>`__                      |                                 |
+-----------------------------------------+---------------------------------+
| `new/6 <#new-6>`__                      |                                 |
+-----------------------------------------+---------------------------------+

Function Details
----------------

add\_appender/2
~~~~~~~~~~~~~~~

``add_appender(GroupId, LoggerId) -> ok``

-  ``GroupId = atom()``
-  ``LoggerId = atom()``

add an appender into the ets

new/3
~~~~~

``new(Id, Appender, Callback) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Appender = log_appender()``
-  ``Callback = module()``

create a logger proc.

new/4
~~~~~

``new(Id, Appender, Callback, Props) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Appender = log_appender()``
-  ``Callback = module()``
-  ``Props = [{atom(), any()}]``

new/5
~~~~~

``new(Id, Appender, Callback, RootPath, FileName) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Appender = log_appender()``
-  ``Callback = module()``
-  ``RootPath = string()``
-  ``FileName = string()``

new/6
~~~~~

``new(Id, Appender, Callback, RootPath, FileName, Level) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Appender = log_appender()``
-  ``Callback = module()``
-  ``RootPath = string()``
-  ``FileName = string()``
-  ``Level = non_neg_integer()``
