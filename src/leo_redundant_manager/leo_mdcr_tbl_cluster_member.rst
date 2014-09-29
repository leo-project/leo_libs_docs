leo\_mdcr\_tbl\_cluster\_member
======================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The multi-datacenter cluster member table's operation.

**References**

-  ```https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_mdcr_tbl_cluster_member.erl`` <https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_mdcr_tbl_cluster_member.erl>`__

Description
-----------

The multi-datacenter cluster member table's operation

Function Index
--------------

+----------------------------------------------------------------+------------------------------------------------+
| `all/0 <#all-0>`__                                             | Retrieve system configuration by cluster-id.   |
+----------------------------------------------------------------+------------------------------------------------+
| `checksum/0 <#checksum-0>`__                                   | Retrieve a checksum by cluster-id.             |
+----------------------------------------------------------------+------------------------------------------------+
| `checksum/1 <#checksum-1>`__                                   |                                                |
+----------------------------------------------------------------+------------------------------------------------+
| `create\_table/2 <#create_table-2>`__                          | Create a table of system-configutation.        |
+----------------------------------------------------------------+------------------------------------------------+
| `delete/1 <#delete-1>`__                                       | Remove members by cluster-id.                  |
+----------------------------------------------------------------+------------------------------------------------+
| `delete\_by\_node/1 <#delete_by_node-1>`__                     | Remove a member by a node.                     |
+----------------------------------------------------------------+------------------------------------------------+
| `find\_by\_cluster\_id/1 <#find_by_cluster_id-1>`__            | Retrieve members by cluster-id.                |
+----------------------------------------------------------------+------------------------------------------------+
| `find\_by\_limit/2 <#find_by_limit-2>`__                       | Retrieve members by limit.                     |
+----------------------------------------------------------------+------------------------------------------------+
| `find\_by\_limit\_with\_rnd/2 <#find_by_limit_with_rnd-2>`__   | Retrieve members by limit.                     |
+----------------------------------------------------------------+------------------------------------------------+
| `find\_by\_node/1 <#find_by_node-1>`__                         | Retrieve a member by a node.                   |
+----------------------------------------------------------------+------------------------------------------------+
| `find\_by\_state/2 <#find_by_state-2>`__                       | Retrieve members by cluseter-id and state.     |
+----------------------------------------------------------------+------------------------------------------------+
| `get/1 <#get-1>`__                                             | Retrieve members by cluster-id.                |
+----------------------------------------------------------------+------------------------------------------------+
| `size/0 <#size-0>`__                                           | Retrieve the records.                          |
+----------------------------------------------------------------+------------------------------------------------+
| `synchronize/1 <#synchronize-1>`__                             | Synchronize records.                           |
+----------------------------------------------------------------+------------------------------------------------+
| `transform/0 <#transform-0>`__                                 | Transform records.                             |
+----------------------------------------------------------------+------------------------------------------------+
| `update/1 <#update-1>`__                                       | Modify a member.                               |
+----------------------------------------------------------------+------------------------------------------------+

Function Details
----------------

all/0
~~~~~

| ``all() -> {ok, [#'?CLUSTER_MEMBER'{}]} | not_found | {error, any()}``

Retrieve system configuration by cluster-id

checksum/0
~~~~~~~~~~

| ``checksum() -> {ok, pos_integer()} | {error, any()}``

Retrieve a checksum by cluster-id

checksum/1
~~~~~~~~~~

``checksum(ClusterId) -> {ok, pos_integer()} | {error, any()}``

-  ``ClusterId = atom()``

create\_table/2
~~~~~~~~~~~~~~~

``create_table(Mode, Nodes) -> ok | {error, any()}``

-  ``Mode = mnesia_copies()``
-  ``Nodes = [atom()]``

Create a table of system-configutation

delete/1
~~~~~~~~

``delete(ClusterId) -> ok | {error, any()}``

-  ``ClusterId = atom()``

Remove members by cluster-id

delete\_by\_node/1
~~~~~~~~~~~~~~~~~~

``delete_by_node(Node) -> ok | {error, any()}``

-  ``Node = atom()``

Remove a member by a node

find\_by\_cluster\_id/1
~~~~~~~~~~~~~~~~~~~~~~~

``find_by_cluster_id(ClusterId) -> {ok, [#'?CLUSTER_MEMBER'{}]} | not_found | {error, any()}``

-  ``ClusterId = atom()``

Retrieve members by cluster-id

find\_by\_limit/2
~~~~~~~~~~~~~~~~~

``find_by_limit(ClusterId, Rows) -> {ok, [#'?CLUSTER_MEMBER'{}]} | not_found | {error, any()}``

-  ``ClusterId = atom()``
-  ``Rows = pos_integer()``

Retrieve members by limit

find\_by\_limit\_with\_rnd/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``find_by_limit_with_rnd(ClusterId, Rows) -> {ok, [#'?CLUSTER_MEMBER'{}]} | not_found | {error, any()}``

-  ``ClusterId = atom()``
-  ``Rows = pos_integer()``

Retrieve members by limit

find\_by\_node/1
~~~~~~~~~~~~~~~~

``find_by_node(Node) -> {ok, #'?CLUSTER_MEMBER'{}} | not_found | {error, any()}``

-  ``Node = atom()``

Retrieve a member by a node

find\_by\_state/2
~~~~~~~~~~~~~~~~~

``find_by_state(ClusterId, State) -> {ok, [#'?CLUSTER_MEMBER'{}]} | not_found | {error, any()}``

-  ``ClusterId = atom()``
-  ``State = node_state()``

Retrieve members by cluseter-id and state

get/1
~~~~~

``get(ClusterId) -> {ok, [#'?CLUSTER_MEMBER'{}]} | not_found | {error, any()}``

-  ``ClusterId = atom()``

Retrieve members by cluster-id

size/0
~~~~~~

| ``size() -> pos_integer()``

Retrieve the records

synchronize/1
~~~~~~~~~~~~~

``synchronize(ValL) -> ok | {error, any()}``

-  ``ValL = [#'?CLUSTER_MEMBER'{}]``

Synchronize records

transform/0
~~~~~~~~~~~

| ``transform() -> ok | {error, any()}``

Transform records

update/1
~~~~~~~~

``update(Member) -> ok | {error, any()}``

-  ``Member = #'?CLUSTER_MEMBER'{}``

Modify a member
