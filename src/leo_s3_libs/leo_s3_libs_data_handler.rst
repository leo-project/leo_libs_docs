leo\_s3\_libs\_data\_handler
===================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

THe s3-libs data handler.

**References**

-  https://github.com/leo-project/leo\_s3\_libs/blob/master/src/leo\_s3\_libs\_data\_handler.erl

Description
-----------

THe s3-libs data handler

Function Index
--------------

+----------------------------+-----------------------------------+
| `all/1 <#all-1>`__         |                                   |
+----------------------------+-----------------------------------+
| `delete/2 <#delete-2>`__   | Remove a record from the table.   |
+----------------------------+-----------------------------------+
| `insert/2 <#insert-2>`__   | Insert a record into the table.   |
+----------------------------+-----------------------------------+
| `lookup/2 <#lookup-2>`__   |                                   |
+----------------------------+-----------------------------------+
| `size/1 <#size-1>`__       | Retrieve total of records.        |
+----------------------------+-----------------------------------+

Function Details
----------------

all/1
~~~~~

``all(DBInfo) -> {ok, [term()]} | not_found | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``

delete/2
~~~~~~~~

``delete(DBInfo, Id) -> ok | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``
-  ``Id = any()``

Remove a record from the table.

insert/2
~~~~~~~~

``insert(DBInfo, X2::{Id, Value}) -> ok | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``
-  ``Id = any()``
-  ``Value = any()``

Insert a record into the table.

lookup/2
~~~~~~~~

``lookup(DBInfo, Id) -> {ok, any()} | not_found | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``
-  ``Id = any()``

size/1
~~~~~~

``size(DBInfo) -> integer()``

-  ``DBInfo = {mnesia | ets, atom()}``

Retrieve total of records.
