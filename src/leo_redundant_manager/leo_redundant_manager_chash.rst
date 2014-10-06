leo\_redundant\_manager\_chash
=====================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The consistent-hashing implementation.

**References**

-  https://github.com/leo-project/leo\_redundant\_manager/blob/master/src/leo\_redundant\_manager\_chash.erl

Description
-----------

The consistent-hashing implementation

Function Index
--------------

+--------------------------------------------------+--------------------------------------+
| `add/2 <#add-2>`__                               | Add a node.                          |
+--------------------------------------------------+--------------------------------------+
| `add\_from\_list/2 <#add_from_list-2>`__         | Insert recods from the list.         |
+--------------------------------------------------+--------------------------------------+
| `checksum/1 <#checksum-1>`__                     | Retrieve ring-checksum.              |
+--------------------------------------------------+--------------------------------------+
| `export/2 <#export-2>`__                         | Dump table to a file.                |
+--------------------------------------------------+--------------------------------------+
| `range\_of\_vnodes/2 <#range_of_vnodes-2>`__     | Retrieve range of vnodes.            |
+--------------------------------------------------+--------------------------------------+
| `redundancies/2 <#redundancies-2>`__             | Retrieve redundancies by vnode-id.   |
+--------------------------------------------------+--------------------------------------+
| `remove/2 <#remove-2>`__                         | Remove a node.                       |
+--------------------------------------------------+--------------------------------------+
| `remove\_from\_list/2 <#remove_from_list-2>`__   | Remove recods from the list.         |
+--------------------------------------------------+--------------------------------------+
| `vnode\_id/1 <#vnode_id-1>`__                    | Retrieve virtual-node-id.            |
+--------------------------------------------------+--------------------------------------+
| `vnode\_id/2 <#vnode_id-2>`__                    |                                      |
+--------------------------------------------------+--------------------------------------+

Function Details
----------------

add/2
~~~~~

``add(TableInfo, Member) -> ok | {error, any()}``

-  ``TableInfo = table_info()``
-  ``Member = #member{}``

Add a node.

add\_from\_list/2
~~~~~~~~~~~~~~~~~

``add_from_list(TableInfo, Members) -> any()``

Insert recods from the list

checksum/1
~~~~~~~~~~

``checksum(TableInfo) -> {ok, integer()}``

-  ``TableInfo = table_info()``

Retrieve ring-checksum

export/2
~~~~~~~~

``export(TableInfo, FileName) -> ok | {error, any()}``

-  ``TableInfo = table_info()``
-  ``FileName = string()``

Dump table to a file.

range\_of\_vnodes/2
~~~~~~~~~~~~~~~~~~~

``range_of_vnodes(TableInfo, VNodeId) -> {ok, [tuple()]}``

-  ``TableInfo = table_info()``
-  ``VNodeId = integer()``

Retrieve range of vnodes.

redundancies/2
~~~~~~~~~~~~~~

``redundancies(TableInfo, VNodeId) -> {ok, #redundancies{}} | not_found``

-  ``TableInfo = table_info()``
-  ``VNodeId = integer()``

Retrieve redundancies by vnode-id.

remove/2
~~~~~~~~

``remove(TableInfo, Member) -> ok | {error, any()}``

-  ``TableInfo = table_info()``
-  ``Member = #member{}``

Remove a node.

remove\_from\_list/2
~~~~~~~~~~~~~~~~~~~~

``remove_from_list(TableInfo, Members) -> ok | {error, any()}``

-  ``TableInfo = table_info()``
-  ``Members = [#member{}]``

Remove recods from the list

vnode\_id/1
~~~~~~~~~~~

``vnode_id(Key) -> integer()``

-  ``Key = any()``

Retrieve virtual-node-id

vnode\_id/2
~~~~~~~~~~~

``vnode_id(X1, Key) -> any()``
