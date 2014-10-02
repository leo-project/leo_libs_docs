leo\_logger\_client\_message
===================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The logger client for handling messages.

**References**

-  https://github.com/leo-project/leo\_logger/blob/master/src/leo\_logger\_client\_message.erl

Description
-----------

The logger client for handling messages

Function Index
--------------

+----------------------------+-------------------------------------+
| `debug/1 <#debug-1>`__     | Output kind of 'Debug log'.         |
+----------------------------+-------------------------------------+
| `error/1 <#error-1>`__     | Output kind of 'Error log'.         |
+----------------------------+-------------------------------------+
| `fatal/1 <#fatal-1>`__     | Output kind of 'Fatal log'.         |
+----------------------------+-------------------------------------+
| `format/2 <#format-2>`__   | Format a log message.               |
+----------------------------+-------------------------------------+
| `info/1 <#info-1>`__       | Output kind of 'Information log'.   |
+----------------------------+-------------------------------------+
| `new/2 <#new-2>`__         | Create loggers for message logs.    |
+----------------------------+-------------------------------------+
| `new/3 <#new-3>`__         |                                     |
+----------------------------+-------------------------------------+
| `warn/1 <#warn-1>`__       | Output kind of 'Warning log'.       |
+----------------------------+-------------------------------------+

Function Details
----------------

debug/1
~~~~~~~

``debug(Log) -> ok``

-  ``Log = #message_log{}``

Output kind of 'Debug log'

error/1
~~~~~~~

``error(Log) -> ok``

-  ``Log = #message_log{}``

Output kind of 'Error log'

fatal/1
~~~~~~~

``fatal(Log) -> ok``

-  ``Log = #message_log{}``

Output kind of 'Fatal log'

format/2
~~~~~~~~

``format(Type, Log) -> string()``

-  ``Type = atom()``
-  ``Log = #message_log{}``

Format a log message

info/1
~~~~~~

``info(Log) -> ok``

-  ``Log = #message_log{}``

Output kind of 'Information log'

new/2
~~~~~

``new(RootPath, Level) -> ok``

-  ``RootPath = string()``
-  ``Level = integer()``

Create loggers for message logs

new/3
~~~~~

``new(RootPath, Level, Loggers) -> ok``

-  ``RootPath = string()``
-  ``Level = integer()``
-  ``Loggers = [{atom(), log_appender()}]``

warn/1
~~~~~~

``warn(Log) -> ok``

-  ``Log = #message_log{}``

Output kind of 'Warning log'
