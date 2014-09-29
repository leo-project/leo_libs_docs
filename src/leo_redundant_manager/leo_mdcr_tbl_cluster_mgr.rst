leo\_mdcr\_tbl\_cluster\_mgr
===================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The multi-datacenter cluster manager talble's operation.

**References**

-  ```https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_mdcr_tbl_cluster_mgr.erl`` <https://github.com/leo-project/leo_redundant_manager/blob/master/src/leo_mdcr_tbl_cluster_mgr.erl>`__

Description
-----------

The multi-datacenter cluster manager talble's operation

Function Index
--------------

+----------------------------------------------+------------------------------------------------+
| `all/0 <#all-0>`__                           | Retrieve system configuration by cluster-id.   |
+----------------------------------------------+------------------------------------------------+
| `checksum/0 <#checksum-0>`__                 | Retrieve a checksum.                           |
+----------------------------------------------+------------------------------------------------+
| `create\_table/2 <#create_table-2>`__        | Create a table of system-configutation.        |
+----------------------------------------------+------------------------------------------------+
| `delete/1 <#delete-1>`__                     | Remove system-configuration.                   |
+----------------------------------------------+------------------------------------------------+
| `delete\_by\_node/1 <#delete_by_node-1>`__   | Remove a node by a node-name.                  |
+----------------------------------------------+------------------------------------------------+
| `get/1 <#get-1>`__                           | Retrieve system configuration by cluster-id.   |
+----------------------------------------------+------------------------------------------------+
| `size/0 <#size-0>`__                         | Retrieve the records.                          |
+----------------------------------------------+------------------------------------------------+
| `synchronize/1 <#synchronize-1>`__           | Synchronize records.                           |
+----------------------------------------------+------------------------------------------------+
| `update/1 <#update-1>`__                     | Modify system-configuration.                   |
+----------------------------------------------+------------------------------------------------+

Function Details
----------------

all/0
~~~~~

| ``all() -> {ok, [#cluster_manager{}]} | not_found | {error, any()}``

Retrieve system configuration by cluster-id

checksum/0
~~~~~~~~~~

| ``checksum() -> {ok, integer()}``

Retrieve a checksum

create\_table/2
~~~~~~~~~~~~~~~

``create_table(Mode, Node) -> ok | {error, any()}``

-  ``Mode = mnesia_copies()``
-  ``Node = [atom()]``

Create a table of system-configutation

delete/1
~~~~~~~~

``delete(ClusterId) -> ok | {error, any()}``

-  ``ClusterId = atom()``

Remove system-configuration

delete\_by\_node/1
~~~~~~~~~~~~~~~~~~

``delete_by_node(Node) -> ok | not_found | {error, any()}``

-  ``Node = atom()``

Remove a node by a node-name

get/1
~~~~~

``get(ClusterId) -> {ok, [#cluster_manager{}]} | not_found | {error, any()}``

-  ``ClusterId = atom()``

Retrieve system configuration by cluster-id

size/0
~~~~~~

| ``size() -> integer()``

Retrieve the records

synchronize/1
~~~~~~~~~~~~~

``synchronize(ValL) -> ok | {error, any()}``

-  ``ValL = [#cluster_manager{}]``

Synchronize records

update/1
~~~~~~~~

``update(ClusterMgr) -> ok | {error, any()}``

-  ``ClusterMgr = #cluster_manager{}``

Modify system-configuration
