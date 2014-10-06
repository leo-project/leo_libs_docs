leo\_mdcr\_tbl\_cluster\_info
====================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The multi-datacenter cluster info table's operation.

**References**

-  https://github.com/leo-project/leo\_redundant\_manager/blob/master/src/leo\_mdcr\_tbl\_cluster\_info.erl

Description
-----------

The multi-datacenter cluster info table's operation

Function Index
--------------

+--------------------------------------------+--------------------------------------------------------------+
| `all/0 <#all-0>`__                         | Retrieve all configuration of remote-clusters.               |
+--------------------------------------------+--------------------------------------------------------------+
| `checksum/0 <#checksum-0>`__               | Retrieve a checksum.                                         |
+--------------------------------------------+--------------------------------------------------------------+
| `create\_table/2 <#create_table-2>`__      | Create a table of configuration of clusters.                 |
+--------------------------------------------+--------------------------------------------------------------+
| `delete/1 <#delete-1>`__                   | Remove a configuration of a cluster.                         |
+--------------------------------------------+--------------------------------------------------------------+
| `find\_by\_limit/1 <#find_by_limit-1>`__   | Retrieve records by limit.                                   |
+--------------------------------------------+--------------------------------------------------------------+
| `get/1 <#get-1>`__                         | Retrieve a configuration of remote-clusters by cluster-id.   |
+--------------------------------------------+--------------------------------------------------------------+
| `size/0 <#size-0>`__                       | Retrieve the records.                                        |
+--------------------------------------------+--------------------------------------------------------------+
| `synchronize/1 <#synchronize-1>`__         | Synchronize records.                                         |
+--------------------------------------------+--------------------------------------------------------------+
| `transform/0 <#transform-0>`__             | Transform records.                                           |
+--------------------------------------------+--------------------------------------------------------------+
| `update/1 <#update-1>`__                   | Modify a configuration of a cluster.                         |
+--------------------------------------------+--------------------------------------------------------------+

Function Details
----------------

all/0
~~~~~

| ``all() -> {ok, [#'?CLUSTER_INFO'{}]} | not_found | {error, any()}``

Retrieve all configuration of remote-clusters

checksum/0
~~~~~~~~~~

| ``checksum() -> {ok, pos_integer()} | {error, any()}``

Retrieve a checksum

create\_table/2
~~~~~~~~~~~~~~~

``create_table(Mode, Nodes) -> ok | {error, any()}``

-  ``Mode = mnesia_copies()``
-  ``Nodes = [atom()]``

Create a table of configuration of clusters

delete/1
~~~~~~~~

``delete(ClusterId) -> ok | {error, any()}``

-  ``ClusterId = atom()``

Remove a configuration of a cluster

find\_by\_limit/1
~~~~~~~~~~~~~~~~~

``find_by_limit(Rows) -> {ok, #'?CLUSTER_INFO'{}} | not_found | {error, any()}``

-  ``Rows = pos_integer()``

Retrieve records by limit

get/1
~~~~~

``get(ClusterId) -> {ok, #'?CLUSTER_INFO'{}} | not_found | {error, any()}``

-  ``ClusterId = atom()``

Retrieve a configuration of remote-clusters by cluster-id

size/0
~~~~~~

| ``size() -> integer()``

Retrieve the records

synchronize/1
~~~~~~~~~~~~~

``synchronize(ValL) -> ok | {error, any()}``

-  ``ValL = [#'?CLUSTER_INFO'{}]``

Synchronize records

transform/0
~~~~~~~~~~~

| ``transform() -> ok | {error, any()}``

Transform records

update/1
~~~~~~~~

``update(ClusterInfo) -> ok | {error, any()}``

-  ``ClusterInfo = #'?CLUSTER_INFO'{}``

Modify a configuration of a cluster
