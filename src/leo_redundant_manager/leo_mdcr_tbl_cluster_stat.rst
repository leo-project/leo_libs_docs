leo\_mdcr\_tbl\_cluster\_stat
====================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The multi-datacenter cluster status talble's operation.

**References**

-  https://github.com/leo-project/leo\_redundant\_manager/blob/master/src/leo\_mdcr\_tbl\_cluster\_stat.erl

Description
-----------

The multi-datacenter cluster status talble's operation

Function Index
--------------

+-------------------------------------------------------+------------------------------------------------+
| `all/0 <#all-0>`__                                    | Retrieve system configuration by cluster-id.   |
+-------------------------------------------------------+------------------------------------------------+
| `checksum/0 <#checksum-0>`__                          | Retrieve a checksum by cluster-id.             |
+-------------------------------------------------------+------------------------------------------------+
| `checksum/1 <#checksum-1>`__                          |                                                |
+-------------------------------------------------------+------------------------------------------------+
| `create\_table/2 <#create_table-2>`__                 | Create a table of system-configutation.        |
+-------------------------------------------------------+------------------------------------------------+
| `delete/1 <#delete-1>`__                              | Remove a cluster-status.                       |
+-------------------------------------------------------+------------------------------------------------+
| `find\_by\_cluster\_id/1 <#find_by_cluster_id-1>`__   | Retrieve system configuration by cluster-id.   |
+-------------------------------------------------------+------------------------------------------------+
| `find\_by\_state/1 <#find_by_state-1>`__              | Retrieve system configuration by State.        |
+-------------------------------------------------------+------------------------------------------------+
| `get/1 <#get-1>`__                                    | Retrieve system configuration by cluster-id.   |
+-------------------------------------------------------+------------------------------------------------+
| `size/0 <#size-0>`__                                  | Retrieve the records.                          |
+-------------------------------------------------------+------------------------------------------------+
| `synchronize/1 <#synchronize-1>`__                    | Synchronize records.                           |
+-------------------------------------------------------+------------------------------------------------+
| `transform/0 <#transform-0>`__                        | Transform records.                             |
+-------------------------------------------------------+------------------------------------------------+
| `update/1 <#update-1>`__                              | Modify system-configuration.                   |
+-------------------------------------------------------+------------------------------------------------+

Function Details
----------------

all/0
~~~~~

| ``all() -> {ok, [#'?CLUSTER_STAT'{}]} | not_found | {error, any()}``

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

Remove a cluster-status

find\_by\_cluster\_id/1
~~~~~~~~~~~~~~~~~~~~~~~

``find_by_cluster_id(ClusterId) -> {ok, #'?CLUSTER_STAT'{}} | not_found | {error, any()}``

-  ``ClusterId = atom()``

Retrieve system configuration by cluster-id

find\_by\_state/1
~~~~~~~~~~~~~~~~~

``find_by_state(State) -> {ok, #'?CLUSTER_STAT'{}} | not_found | {error, any()}``

-  ``State = atom()``

Retrieve system configuration by State

get/1
~~~~~

``get(ClusterId) -> {ok, #'?CLUSTER_STAT'{}} | not_found | {error, any()}``

-  ``ClusterId = atom()``

Retrieve system configuration by cluster-id

size/0
~~~~~~

| ``size() -> pos_integer()``

Retrieve the records

synchronize/1
~~~~~~~~~~~~~

| ``synchronize(Vals::list()) -> ok | {error, any()}``

Synchronize records

transform/0
~~~~~~~~~~~

| ``transform() -> ok | {error, any()}``

Transform records

update/1
~~~~~~~~

``update(ClusterStat) -> ok | {error, any()}``

-  ``ClusterStat = #'?CLUSTER_STAT'{}``

Modify system-configuration
