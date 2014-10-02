leo\_logger\_appender\_file
==================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The file appender.

**Behaviours:** ```leo_logger_behavior`` <leo_logger_behavior.html>`__.

**References**

-  https://github.com/leo-project/leo\_logger/blob/master/src/leo\_logger\_appender\_file.erl

Description
-----------

The file appender

Function Index
--------------

+---------------------------------------+-------------------------------+
| `append/2 <#append-2>`__              | Append a message to a file.   |
+---------------------------------------+-------------------------------+
| `bulk\_output/2 <#bulk_output-2>`__   | Output messages.              |
+---------------------------------------+-------------------------------+
| `close/1 <#close-1>`__                | Close the log file.           |
+---------------------------------------+-------------------------------+
| `format/2 <#format-2>`__              | Format a log message.         |
+---------------------------------------+-------------------------------+
| `init/3 <#init-3>`__                  | Initialize the logger.        |
+---------------------------------------+-------------------------------+
| `rotate/2 <#rotate-2>`__              | Rotate the log file.          |
+---------------------------------------+-------------------------------+
| `sync/1 <#sync-1>`__                  | Synchronize the file.         |
+---------------------------------------+-------------------------------+

Function Details
----------------

append/2
~~~~~~~~

``append(Msg, State) -> #logger_state{}``

-  ``Msg = #message_log{}``
-  ``State = #logger_state{}``

Append a message to a file

bulk\_output/2
~~~~~~~~~~~~~~

``bulk_output(Logs, State) -> #logger_state{}``

-  ``Logs = [term()]``
-  ``State = #logger_state{}``

Output messages

close/1
~~~~~~~

``close(State) -> ok | {error, any()}``

-  ``State = #logger_state{}``

Close the log file

format/2
~~~~~~~~

``format(Type, Msg) -> Ret``

-  ``Type = split | bulk``
-  ``Msg = #message_log{}``
-  ``Ret = string()``

Format a log message

init/3
~~~~~~

``init(Appender, CallbackMod, Props) -> {ok, #logger_state{}} | {error, term()}``

-  ``Appender = atom()``
-  ``CallbackMod = module()``
-  ``Props = [{atom(), any()}]``

Initialize the logger

rotate/2
~~~~~~~~

``rotate(Hours, State) -> {ok, #logger_state{}}``

-  ``Hours = {integer(), integer(), integer(), integer()}``
-  ``State = #logger_state{}``

Rotate the log file

sync/1
~~~~~~

``sync(State) -> ok | {error, term()}``

-  ``State = #logger_state{}``

Synchronize the file
