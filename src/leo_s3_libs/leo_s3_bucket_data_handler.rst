leo\_s3\_bucket\_data\_handler
=====================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The bucket record handler.

**References**

-  https://github.com/leo-project/leo\_s3\_libs/blob/master/src/leo\_s3\_bucket\_data\_handler.erl

Description
-----------

The bucket record handler

Function Index
--------------

+------------------------------------------+-----------------------------------+
| `delete/2 <#delete-2>`__                 | Remove a record from the table.   |
+------------------------------------------+-----------------------------------+
| `find\_all/1 <#find_all-1>`__            | Retrieve all buckets.             |
+------------------------------------------+-----------------------------------+
| `find\_by\_name/2 <#find_by_name-2>`__   | Retrieve a record by name.        |
+------------------------------------------+-----------------------------------+
| `find\_by\_name/3 <#find_by_name-3>`__   |                                   |
+------------------------------------------+-----------------------------------+
| `find\_by\_name/4 <#find_by_name-4>`__   |                                   |
+------------------------------------------+-----------------------------------+
| `insert/2 <#insert-2>`__                 | Insert a record into the table.   |
+------------------------------------------+-----------------------------------+
| `lookup/2 <#lookup-2>`__                 |                                   |
+------------------------------------------+-----------------------------------+
| `size/1 <#size-1>`__                     | Retrieve total of records.        |
+------------------------------------------+-----------------------------------+

Function Details
----------------

delete/2
~~~~~~~~

``delete(DBInfo, Bucket) -> ok | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``
-  ``Bucket = #'?BUCKET'{}``

Remove a record from the table.

find\_all/1
~~~~~~~~~~~

``find_all(DBInfo) -> {ok, [#'?BUCKET'{}]} | not_found | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``

Retrieve all buckets.

find\_by\_name/2
~~~~~~~~~~~~~~~~

``find_by_name(DBInfo, Name) -> {ok, #'?BUCKET'{}} | not_found | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``
-  ``Name = binary()``

Retrieve a record by name

find\_by\_name/3
~~~~~~~~~~~~~~~~

``find_by_name(DBInfo, AccessKey, Name) -> {ok, #'?BUCKET'{}} | not_found | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``
-  ``AccessKey = binary()``
-  ``Name = binary()``

find\_by\_name/4
~~~~~~~~~~~~~~~~

``find_by_name(DBInfo, AccessKey0, Name, NeedAccessKey) -> {ok, #'?BUCKET'{}} | not_found | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``
-  ``AccessKey0 = binary()``
-  ``Name = binary()``
-  ``NeedAccessKey = boolean()``

insert/2
~~~~~~~~

``insert(DBInfo, Bucket) -> ok | {error, any()}``

-  ``DBInfo = {mnesia | ets, atom()}``
-  ``Bucket = #'?BUCKET'{}``

Insert a record into the table.

lookup/2
~~~~~~~~

``lookup(X1::{DB, Table}, AccessKey) -> {ok, [#'?BUCKET'{}]} | not_found | {error, any()}``

-  ``DB = mnesia | ets``
-  ``Table = atom()``
-  ``AccessKey = binary()``

size/1
~~~~~~

``size(DBInfo) -> non_neg_integer()``

-  ``DBInfo = {mnesia | ets, atom()}``

Retrieve total of records.
