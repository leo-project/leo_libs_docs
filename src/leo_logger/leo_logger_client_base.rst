leo\_logger\_client\_base
================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The base of logger client.

**References**

-  https://github.com/leo-project/leo\_logger/blob/master/src/leo\_logger\_client\_base.erl

Description
-----------

The base of logger client

Function Index
--------------

+---------------------------------------------+------------------------------------+
| `append/1 <#append-1>`__                    | Append a message to a file.        |
+---------------------------------------------+------------------------------------+
| `force\_rotation/1 <#force_rotation-1>`__   | Force log-rotation.                |
+---------------------------------------------+------------------------------------+
| `format/2 <#format-2>`__                    | Format a log message.              |
+---------------------------------------------+------------------------------------+
| `new/4 <#new-4>`__                          | Create loggers for message logs.   |
+---------------------------------------------+------------------------------------+
| `sync/1 <#sync-1>`__                        | Sync a log file.                   |
+---------------------------------------------+------------------------------------+

Function Details
----------------

append/1
~~~~~~~~

``append(LogInfo) -> ok``

-  ``LogInfo = {atom(), #message_log{}}``

Append a message to a file

force\_rotation/1
~~~~~~~~~~~~~~~~~

``force_rotation(LogId) -> ok | {error, term()}``

-  ``LogId = atom()``

Force log-rotation

format/2
~~~~~~~~

``format(Appender, Log) -> string()``

-  ``Appender = atom()``
-  ``Log = #message_log{}``

Format a log message

new/4
~~~~~

``new(LogGroup, LogId, RootPath, LogFileName) -> ok``

-  ``LogGroup = atom()``
-  ``LogId = atom()``
-  ``RootPath = string()``
-  ``LogFileName = string()``

Create loggers for message logs

sync/1
~~~~~~

``sync(LogId) -> ok | {error, term()}``

-  ``LogId = atom() | #logger_state{}``

Sync a log file
