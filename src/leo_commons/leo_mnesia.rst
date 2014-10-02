leo\_mnesia
==================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_mnesia is utilities for mnesia operation.

**References**

-  ```https://github.com/leo-project/leo_commons/blob/master/src/leo_mnesia.erl`` <https://github.com/leo-project/leo_commons/blob/master/src/leo_mnesia.erl>`__

Description
-----------

leo\_mnesia is utilities for mnesia operation

Function Index
--------------

+----------------------------+---------------------------------+
| `delete/1 <#delete-1>`__   | Remove a value from mnesia.     |
+----------------------------+---------------------------------+
| `export/2 <#export-2>`__   | Export mnesia's records.        |
+----------------------------+---------------------------------+
| `export/3 <#export-3>`__   | Export mnesia's records.        |
+----------------------------+---------------------------------+
| `read/1 <#read-1>`__       | Retrieve a value from mnesia.   |
+----------------------------+---------------------------------+
| `write/1 <#write-1>`__     | Insert a value into mnesia.     |
+----------------------------+---------------------------------+

Function Details
----------------

delete/1
~~~~~~~~

``delete(Fun) -> ok | {error, any()}``

-  ``Fun = function()``

Remove a value from mnesia

export/2
~~~~~~~~

``export(FilePath, Table) -> ok | {error, any()}``

-  ``FilePath = string()``
-  ``Table = atom()``

Export mnesia's records

export/3
~~~~~~~~

``export(FilePath, Table, ExportType) -> ok | {error, any()}``

-  ``FilePath = string()``
-  ``Table = atom()``
-  ``ExportType = export_type()``

Export mnesia's records

read/1
~~~~~~

``read(Fun) -> {ok, [any()]} | not_found | {error, any()}``

-  ``Fun = function()``

Retrieve a value from mnesia

write/1
~~~~~~~

``write(Fun) -> ok | {error, any()}``

-  ``Fun = function()``

Insert a value into mnesia
