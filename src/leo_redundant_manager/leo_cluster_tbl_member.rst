leo\_cluster\_tbl\_member
================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The cluster member table operation.

**References**

-  ```https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_cluster_tbl_member.erl`` <https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_cluster_tbl_member.erl>`__

Description
-----------

The cluster member table operation

Function Index
--------------

+----------------------------------------------+------------------------------------------------+
| `create\_table/1 <#create_table-1>`__        | Create the member table.                       |
+----------------------------------------------+------------------------------------------------+
| `create\_table/3 <#create_table-3>`__        |                                                |
+----------------------------------------------+------------------------------------------------+
| `delete/1 <#delete-1>`__                     | Remove a record from the table.                |
+----------------------------------------------+------------------------------------------------+
| `delete/2 <#delete-2>`__                     |                                                |
+----------------------------------------------+------------------------------------------------+
| `delete/3 <#delete-3>`__                     |                                                |
+----------------------------------------------+------------------------------------------------+
| `delete\_all/1 <#delete_all-1>`__            | Remove all records.                            |
+----------------------------------------------+------------------------------------------------+
| `delete\_all/2 <#delete_all-2>`__            |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_all/0 <#find_all-0>`__                | Retrieve all members from the table.           |
+----------------------------------------------+------------------------------------------------+
| `find\_all/1 <#find_all-1>`__                |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_all/2 <#find_all-2>`__                |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_alias/1 <#find_by_alias-1>`__     | Retrieve records by alias.                     |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_alias/2 <#find_by_alias-2>`__     |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_alias/3 <#find_by_alias-3>`__     |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_level1/2 <#find_by_level1-2>`__   | Retrieve records by L1 and L2.                 |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_level1/3 <#find_by_level1-3>`__   |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_level1/4 <#find_by_level1-4>`__   |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_level2/1 <#find_by_level2-1>`__   | Retrieve records by L2.                        |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_level2/2 <#find_by_level2-2>`__   |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_level2/3 <#find_by_level2-3>`__   |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_name/2 <#find_by_name-2>`__       | Retrieve records by name.                      |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_name/3 <#find_by_name-3>`__       |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_status/1 <#find_by_status-1>`__   | Retrieve members by status.                    |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_status/2 <#find_by_status-2>`__   |                                                |
+----------------------------------------------+------------------------------------------------+
| `find\_by\_status/3 <#find_by_status-3>`__   |                                                |
+----------------------------------------------+------------------------------------------------+
| `first/1 <#first-1>`__                       |                                                |
+----------------------------------------------+------------------------------------------------+
| `insert/1 <#insert-1>`__                     | Insert a record into the table.                |
+----------------------------------------------+------------------------------------------------+
| `insert/2 <#insert-2>`__                     |                                                |
+----------------------------------------------+------------------------------------------------+
| `insert/3 <#insert-3>`__                     |                                                |
+----------------------------------------------+------------------------------------------------+
| `lookup/1 <#lookup-1>`__                     | Retrieve a record by key from the table.       |
+----------------------------------------------+------------------------------------------------+
| `lookup/2 <#lookup-2>`__                     |                                                |
+----------------------------------------------+------------------------------------------------+
| `lookup/3 <#lookup-3>`__                     |                                                |
+----------------------------------------------+------------------------------------------------+
| `next/2 <#next-2>`__                         |                                                |
+----------------------------------------------+------------------------------------------------+
| `overwrite/2 <#overwrite-2>`__               | Overwrite current records by source records.   |
+----------------------------------------------+------------------------------------------------+
| `replace/2 <#replace-2>`__                   | Replace members into the db.                   |
+----------------------------------------------+------------------------------------------------+
| `replace/3 <#replace-3>`__                   |                                                |
+----------------------------------------------+------------------------------------------------+
| `replace/4 <#replace-4>`__                   |                                                |
+----------------------------------------------+------------------------------------------------+
| `tab2list/0 <#tab2list-0>`__                 | Retrieve list from the table.                  |
+----------------------------------------------+------------------------------------------------+
| `tab2list/1 <#tab2list-1>`__                 |                                                |
+----------------------------------------------+------------------------------------------------+
| `tab2list/2 <#tab2list-2>`__                 |                                                |
+----------------------------------------------+------------------------------------------------+
| `table\_size/0 <#table_size-0>`__            | Retrieve total of records.                     |
+----------------------------------------------+------------------------------------------------+
| `table\_size/1 <#table_size-1>`__            |                                                |
+----------------------------------------------+------------------------------------------------+
| `table\_size/2 <#table_size-2>`__            |                                                |
+----------------------------------------------+------------------------------------------------+
| `transform/0 <#transform-0>`__               | Transform records.                             |
+----------------------------------------------+------------------------------------------------+
| `transform/1 <#transform-1>`__               |                                                |
+----------------------------------------------+------------------------------------------------+

Function Details
----------------

create\_table/1
~~~~~~~~~~~~~~~

``create_table(Table) -> ok``

-  ``Table = member_table()``

Create the member table.

create\_table/3
~~~~~~~~~~~~~~~

``create_table(DiscCopy, Nodes, Table) -> ok``

-  ``DiscCopy = mnesia_copies()``
-  ``Nodes = [atom()]``
-  ``Table = member_table()``

delete/1
~~~~~~~~

``delete(Node) -> ok | {error, any}``

-  ``Node = atom()``

Remove a record from the table.

delete/2
~~~~~~~~

``delete(Table, Node) -> ok | {error, any}``

-  ``Table = member_table()``
-  ``Node = atom()``

delete/3
~~~~~~~~

``delete(DBType, Table, Node) -> ok | {error, any}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = member_table()``
-  ``Node = atom()``

delete\_all/1
~~~~~~~~~~~~~

``delete_all(Table) -> ok | {error, any()}``

-  ``Table = member_table()``

Remove all records

delete\_all/2
~~~~~~~~~~~~~

``delete_all(DBType, Table) -> ok | {error, any()}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = member_table()``

find\_all/0
~~~~~~~~~~~

| ``find_all() -> {ok, [#member{}]} | not_found | {error, any()}``

Retrieve all members from the table.

find\_all/1
~~~~~~~~~~~

``find_all(Table) -> {ok, [#member{}]} | not_found | {error, any()}``

-  ``Table = member_table()``

find\_all/2
~~~~~~~~~~~

``find_all(DBType, Table) -> {ok, [#member{}]} | not_found | {error, any()}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = member_table()``

find\_by\_alias/1
~~~~~~~~~~~~~~~~~

``find_by_alias(Alias) -> {ok, list()} | not_found | {error, any()}``

-  ``Alias = string()``

Retrieve records by alias

find\_by\_alias/2
~~~~~~~~~~~~~~~~~

``find_by_alias(Table, Alias) -> {ok, list()} | not_found | {error, any()}``

-  ``Table = atom()``
-  ``Alias = string()``

find\_by\_alias/3
~~~~~~~~~~~~~~~~~

``find_by_alias(DBType, Table, Alias) -> {ok, list()} | not_found | {error, any()}``

-  ``DBType = '?DB_MNESIA' | '?DB_ETS'``
-  ``Table = atom()``
-  ``Alias = string()``

find\_by\_level1/2
~~~~~~~~~~~~~~~~~~

``find_by_level1(L1, L2) -> {ok, list()} | not_found | {error, any()}``

-  ``L1 = atom()``
-  ``L2 = atom()``

Retrieve records by L1 and L2

find\_by\_level1/3
~~~~~~~~~~~~~~~~~~

``find_by_level1(Table, L1, L2) -> {ok, list()} | not_found | {error, any()}``

-  ``Table = member_table()``
-  ``L1 = atom()``
-  ``L2 = atom()``

find\_by\_level1/4
~~~~~~~~~~~~~~~~~~

``find_by_level1(DBType, Table, L1, L2) -> {ok, list()} | not_found | {error, any()}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = member_table()``
-  ``L1 = atom()``
-  ``L2 = atom()``

find\_by\_level2/1
~~~~~~~~~~~~~~~~~~

``find_by_level2(L2) -> {ok, list()} | not_found | {error, any()}``

-  ``L2 = atom()``

Retrieve records by L2

find\_by\_level2/2
~~~~~~~~~~~~~~~~~~

``find_by_level2(Table, L2) -> {ok, list()} | not_found | {error, any()}``

-  ``Table = member_table()``
-  ``L2 = atom()``

find\_by\_level2/3
~~~~~~~~~~~~~~~~~~

``find_by_level2(DBType, Table, L2) -> {ok, list()} | not_found | {error, any()}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = member_table()``
-  ``L2 = atom()``

find\_by\_name/2
~~~~~~~~~~~~~~~~

``find_by_name(Table, Name) -> {ok, list()} | not_found | {error, any()}``

-  ``Table = atom()``
-  ``Name = atom()``

Retrieve records by name

find\_by\_name/3
~~~~~~~~~~~~~~~~

``find_by_name(DBType, Table, Name) -> {ok, list()} | not_found | {error, any()}``

-  ``DBType = '?DB_MNESIA' | '?DB_ETS'``
-  ``Table = atom()``
-  ``Name = atom()``

find\_by\_status/1
~~~~~~~~~~~~~~~~~~

``find_by_status(Status) -> {ok, [#member{}]} | not_found | {error, any()}``

-  ``Status = atom()``

Retrieve members by status

find\_by\_status/2
~~~~~~~~~~~~~~~~~~

``find_by_status(Table, Status) -> {ok, [#member{}]} | not_found | {error, any()}``

-  ``Table = member_table()``
-  ``Status = atom()``

find\_by\_status/3
~~~~~~~~~~~~~~~~~~

``find_by_status(DBType, Table, Status) -> {ok, [#member{}]} | not_found | {error, any()}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = member_table()``
-  ``Status = atom()``

first/1
~~~~~~~

``first(Table) -> atom() | '$end_of_table'``

-  ``Table = atom()``

insert/1
~~~~~~~~

``insert(Record) -> ok | {error, any}``

-  ``Record = {atom(), #member{}}``

Insert a record into the table.

insert/2
~~~~~~~~

``insert(Table, Record) -> ok | {error, any}``

-  ``Table = member_table()``
-  ``Record = {atom(), #member{}}``

insert/3
~~~~~~~~

``insert(DBType, Table, Record) -> ok | {error, any}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = member_table()``
-  ``Record = {atom(), #member{}}``

lookup/1
~~~~~~~~

``lookup(Node) -> {ok, #member{}} | not_found | {error, any()}``

-  ``Node = atom()``

Retrieve a record by key from the table.

lookup/2
~~~~~~~~

``lookup(Table, Node) -> {ok, #member{}} | not_found | {error, any()}``

-  ``Table = atom()``
-  ``Node = atom()``

lookup/3
~~~~~~~~

``lookup(DBType, Table, Node) -> {ok, #member{}} | not_found | {error, any()}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = atom()``
-  ``Node = atom()``

next/2
~~~~~~

``next(Table, MemberName) -> atom() | '$end_of_table'``

-  ``Table = atom()``
-  ``MemberName = atom()``

overwrite/2
~~~~~~~~~~~

``overwrite(SrcTable, DestTable) -> ok | {error, any()}``

-  ``SrcTable = member_table()``
-  ``DestTable = member_table()``

Overwrite current records by source records

replace/2
~~~~~~~~~

``replace(OldMembers, NewMembers) -> ok``

-  ``OldMembers = [#member{}]``
-  ``NewMembers = [#member{}]``

Replace members into the db.

replace/3
~~~~~~~~~

``replace(Table, OldMembers, NewMembers) -> ok``

-  ``Table = member_table()``
-  ``OldMembers = [#member{}]``
-  ``NewMembers = [#member{}]``

replace/4
~~~~~~~~~

``replace(DBType, Table, OldMembers, NewMembers) -> ok``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = member_table()``
-  ``OldMembers = [#member{}]``
-  ``NewMembers = [#member{}]``

tab2list/0
~~~~~~~~~~

| ``tab2list() -> list() | {error, any()}``

Retrieve list from the table.

tab2list/1
~~~~~~~~~~

``tab2list(Table) -> list() | {error, any()}``

-  ``Table = member_table()``

tab2list/2
~~~~~~~~~~

``tab2list(DBType, Table) -> list() | {error, any()}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = member_table()``

table\_size/0
~~~~~~~~~~~~~

| ``table_size() -> integer() | {error, any()}``

Retrieve total of records.

table\_size/1
~~~~~~~~~~~~~

``table_size(Table) -> integer() | {error, any()}``

-  ``Table = atom()``

table\_size/2
~~~~~~~~~~~~~

``table_size(DBType, Table) -> integer() | {error, any()}``

-  ``DBType = '?DB_ETS' | '?DB_MNESIA'``
-  ``Table = atom()``

transform/0
~~~~~~~~~~~

| ``transform() -> ok | {error, any()}``

Transform records

transform/1
~~~~~~~~~~~

``transform(MnesiaNodes) -> ok | {error, any()}``

-  ``MnesiaNodes = [atom()]``
