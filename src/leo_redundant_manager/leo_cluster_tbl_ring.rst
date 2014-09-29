leo\_cluster\_tbl\_ring
==============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The cluster ring table's operation.

**References**

-  ```https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_cluster_tbl_ring.erl`` <https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_cluster_tbl_ring.erl>`__

Description
-----------

The cluster ring table's operation

Function Index
--------------

+-------------------------------------------------------------+------------------------------------------------+
| `bulk\_delete/2 <#bulk_delete-2>`__                         | Remove bulk of records from the table.         |
+-------------------------------------------------------------+------------------------------------------------+
| `bulk\_insert/2 <#bulk_insert-2>`__                         | Insert bulk of records into the table.         |
+-------------------------------------------------------------+------------------------------------------------+
| `create\_table\_current/1 <#create_table_current-1>`__      | create ring-current table.                     |
+-------------------------------------------------------------+------------------------------------------------+
| `create\_table\_current/2 <#create_table_current-2>`__      |                                                |
+-------------------------------------------------------------+------------------------------------------------+
| `create\_table\_for\_test/3 <#create_table_for_test-3>`__   | create table for the test.                     |
+-------------------------------------------------------------+------------------------------------------------+
| `create\_table\_prev/1 <#create_table_prev-1>`__            | create ring-prev table.                        |
+-------------------------------------------------------------+------------------------------------------------+
| `create\_table\_prev/2 <#create_table_prev-2>`__            |                                                |
+-------------------------------------------------------------+------------------------------------------------+
| `delete/2 <#delete-2>`__                                    | Remove a record from the table.                |
+-------------------------------------------------------------+------------------------------------------------+
| `delete\_all/1 <#delete_all-1>`__                           | Remove all objects from the table.             |
+-------------------------------------------------------------+------------------------------------------------+
| `first/1 <#first-1>`__                                      | Retrieve a first record from the table.        |
+-------------------------------------------------------------+------------------------------------------------+
| `insert/2 <#insert-2>`__                                    | Insert a record into the table.                |
+-------------------------------------------------------------+------------------------------------------------+
| `last/1 <#last-1>`__                                        | Retrieve a last record from the table.         |
+-------------------------------------------------------------+------------------------------------------------+
| `lookup/2 <#lookup-2>`__                                    | Retrieve a record by key from the table.       |
+-------------------------------------------------------------+------------------------------------------------+
| `next/2 <#next-2>`__                                        | Retrieve a next record from the table.         |
+-------------------------------------------------------------+------------------------------------------------+
| `overwrite/2 <#overwrite-2>`__                              | Overwrite current records by source records.   |
+-------------------------------------------------------------+------------------------------------------------+
| `prev/2 <#prev-2>`__                                        | Retrieve a previous record from the table.     |
+-------------------------------------------------------------+------------------------------------------------+
| `size/1 <#size-1>`__                                        | Retrieve total of records.                     |
+-------------------------------------------------------------+------------------------------------------------+
| `tab2list/1 <#tab2list-1>`__                                | Retrieve list from the table.                  |
+-------------------------------------------------------------+------------------------------------------------+

Function Details
----------------

bulk\_delete/2
~~~~~~~~~~~~~~

``bulk_delete(TableInfo, List) -> ok | {error, any()}``

-  ``TableInfo = table_info()``
-  ``List = [integer()]``

Remove bulk of records from the table

bulk\_insert/2
~~~~~~~~~~~~~~

``bulk_insert(TableInfo, List) -> ok | {error, any()}``

-  ``TableInfo = table_info()``
-  ``List = [{integer(), atom(), integer()}]``

Insert bulk of records into the table

create\_table\_current/1
~~~~~~~~~~~~~~~~~~~~~~~~

``create_table_current(Mode) -> ok``

-  ``Mode = mnesia_copies()``

create ring-current table

create\_table\_current/2
~~~~~~~~~~~~~~~~~~~~~~~~

``create_table_current(Mode, Nodes) -> ok``

-  ``Mode = mnesia_copies()``
-  ``Nodes = [atom()]``

create\_table\_for\_test/3
~~~~~~~~~~~~~~~~~~~~~~~~~~

``create_table_for_test(Mode, Nodes, Table) -> any()``

create table for the test

create\_table\_prev/1
~~~~~~~~~~~~~~~~~~~~~

``create_table_prev(Mode) -> ok``

-  ``Mode = mnesia_copies()``

create ring-prev table

create\_table\_prev/2
~~~~~~~~~~~~~~~~~~~~~

``create_table_prev(Mode, Nodes) -> ok``

-  ``Mode = mnesia_copies()``
-  ``Nodes = [atom()]``

delete/2
~~~~~~~~

``delete(TableInfo, VNodeId) -> ok | {error, any()}``

-  ``TableInfo = table_info()``
-  ``VNodeId = integer()``

Remove a record from the table

delete\_all/1
~~~~~~~~~~~~~

``delete_all(TableInfo) -> ok``

-  ``TableInfo = table_info()``

Remove all objects from the table

first/1
~~~~~~~

``first(TableInfo) -> integer() | '$end_of_table'``

-  ``TableInfo = table_info()``

Retrieve a first record from the table

insert/2
~~~~~~~~

``insert(TableInfo, Ring) -> ok | {error, any()}``

-  ``TableInfo = table_info()``
-  ``Ring = #ring{} | #ring_0_16_8{} | tuple()``

Insert a record into the table

last/1
~~~~~~

``last(TableInfo) -> integer() | '$end_of_table'``

-  ``TableInfo = table_info()``

Retrieve a last record from the table

lookup/2
~~~~~~~~

``lookup(TableInfo, VNodeId) -> #'?RING'{} | not_found | {error, any()}``

-  ``TableInfo = table_info()``
-  ``VNodeId = integer()``

Retrieve a record by key from the table

next/2
~~~~~~

| ``next(X1::{'?DB_MNESIA' | '?DB_ETS', atom()}, VNodeId::integer()) -> integer() | '$end_of_table'``

Retrieve a next record from the table

overwrite/2
~~~~~~~~~~~

``overwrite(TableInfo, TableInfo) -> ok | {error, any()}``

-  ``TableInfo = table_info()``

Overwrite current records by source records

prev/2
~~~~~~

``prev(TableInfo, VNodeId) -> integer() | '$end_of_table'``

-  ``TableInfo = table_info()``
-  ``VNodeId = integer()``

Retrieve a previous record from the table

size/1
~~~~~~

``size(TableInfo) -> integer()``

-  ``TableInfo = table_info()``

Retrieve total of records

tab2list/1
~~~~~~~~~~

``tab2list(TableInfo) -> [tuple()] | [#'?RING'{}] | {error, any()}``

-  ``TableInfo = table_info()``

Retrieve list from the table
