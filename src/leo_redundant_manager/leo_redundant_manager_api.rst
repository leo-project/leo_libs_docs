leo\_redundant\_manager\_api
===================================

-  `Description <#description>`__
-  `Data Types <#types>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_redaundant\_manager's API.

**References**

-  https://github.com/leo-project/leo\_redundant\_manager/blob/master/src/leo\_redundant\_manager\_api.erl

Description
-----------

leo\_redaundant\_manager's API

Data Types
----------

method()
~~~~~~~~

``method() = put | get | delete | head | default``

Function Index
--------------

+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `attach/1 <#attach-1>`__                                                 | attach a node.                                                        |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `attach/2 <#attach-2>`__                                                 |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `attach/3 <#attach-3>`__                                                 |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `attach/4 <#attach-4>`__                                                 |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `attach/5 <#attach-5>`__                                                 |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `checksum/1 <#checksum-1>`__                                             | get routing\_table's checksum.                                        |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `create/0 <#create-0>`__                                                 | Create the RING.                                                      |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `create/1 <#create-1>`__                                                 |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `create/2 <#create-2>`__                                                 |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `create/3 <#create-3>`__                                                 |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `delete\_member\_by\_node/1 <#delete_member_by_node-1>`__                | remove a member by node-name.                                         |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `detach/1 <#detach-1>`__                                                 | detach a node.                                                        |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `detach/2 <#detach-2>`__                                                 |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `dump/1 <#dump-1>`__                                                     | Dump table-records.                                                   |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `force\_sync\_workers/0 <#force_sync_workers-0>`__                       | Force sync ring-workers.                                              |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_alias/2 <#get_alias-2>`__                                          | Generate an alias of the node.                                        |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_alias/3 <#get_alias-3>`__                                          |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_alias/4 <#get_alias-4>`__                                          |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_cluster\_status/0 <#get_cluster_status-0>`__                       | Retrieve local cluster's status.                                      |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_cluster\_tbl\_checksums/0 <#get_cluster_tbl_checksums-0>`__        | Retrieve checksums of cluster-related tables.                         |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_member\_by\_node/1 <#get_member_by_node-1>`__                      | get a member by node-name.                                            |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_members/0 <#get_members-0>`__                                      | get members.                                                          |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_members/1 <#get_members-1>`__                                      |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_members\_by\_status/1 <#get_members_by_status-1>`__                | get members by status.                                                |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_members\_by\_status/2 <#get_members_by_status-2>`__                |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_members\_count/0 <#get_members_count-0>`__                         | get # of members.                                                     |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_options/0 <#get_options-0>`__                                      | get routing-table's options.                                          |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_redundancies\_by\_addr\_id/1 <#get_redundancies_by_addr_id-1>`__   | Retrieve redundancies from the ring-table.                            |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_redundancies\_by\_addr\_id/2 <#get_redundancies_by_addr_id-2>`__   |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_redundancies\_by\_key/1 <#get_redundancies_by_key-1>`__            | Retrieve redundancies from the ring-table.                            |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_redundancies\_by\_key/2 <#get_redundancies_by_key-2>`__            |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_remote\_clusters/0 <#get_remote_clusters-0>`__                     | Retrieve conf of remote clusters.                                     |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_remote\_clusters/1 <#get_remote_clusters-1>`__                     |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_remote\_members/1 <#get_remote_members-1>`__                       | Retrieve remote cluster members.                                      |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_remote\_members/2 <#get_remote_members-2>`__                       |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_ring/0 <#get_ring-0>`__                                            | Retrieve Ring.                                                        |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `get\_ring/1 <#get_ring-1>`__                                            |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `has\_charge\_of\_node/2 <#has_charge_of_node-2>`__                      | Has charge of node? 'true' is returned even if it detects an error.   |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `has\_member/1 <#has_member-1>`__                                        | Has a member ?.                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `is\_alive/0 <#is_alive-0>`__                                            | Is alive the process?.                                                |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `range\_of\_vnodes/1 <#range_of_vnodes-1>`__                             | Retrieve range of vnodes.                                             |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `rebalance/0 <#rebalance-0>`__                                           | Re-balance objects in the cluster.                                    |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `reserve/3 <#reserve-3>`__                                               | reserve a node during in operation.                                   |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `reserve/5 <#reserve-5>`__                                               |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `reserve/6 <#reserve-6>`__                                               |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `set\_options/1 <#set_options-1>`__                                      | set routing-table's options.                                          |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `suspend/1 <#suspend-1>`__                                               | suspend a node.                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `suspend/2 <#suspend-2>`__                                               |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `synchronize/2 <#synchronize-2>`__                                       | synchronize member-list and routing-table.                            |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `synchronize/3 <#synchronize-3>`__                                       | synchronize member-list and routing-table.                            |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `table\_info/1 <#table_info-1>`__                                        | Retrieve table-info by version.                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `table\_info/1 <#table_info-1>`__                                        |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `update\_member/1 <#update_member-1>`__                                  | update members.                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `update\_member\_by\_node/2 <#update_member_by_node-2>`__                | update a member by node-name.                                         |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `update\_member\_by\_node/3 <#update_member_by_node-3>`__                |                                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `update\_members/1 <#update_members-1>`__                                | update members.                                                       |
+--------------------------------------------------------------------------+-----------------------------------------------------------------------+

Function Details
----------------

attach/1
~~~~~~~~

``attach(Node) -> ok | {error, any()}``

-  ``Node = atom()``

attach a node.

attach/2
~~~~~~~~

``attach(Node, AwarenessL2) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``AwarenessL2 = string()``

attach/3
~~~~~~~~

``attach(Node, AwarenessL2, Clock) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``

attach/4
~~~~~~~~

``attach(Node, AwarenessL2, Clock, NumOfVNodes) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``
-  ``NumOfVNodes = integer()``

attach/5
~~~~~~~~

``attach(Node, AwarenessL2, Clock, NumOfVNodes, RPCPort) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``
-  ``NumOfVNodes = integer()``
-  ``RPCPort = integer()``

checksum/1
~~~~~~~~~~

``checksum(Type) -> {ok, integer()} | {ok, {integer(), integer()}} | {error, any()}``

-  ``Type = '?CHECKSUM_RING' | '?CHECKSUM_MEMBER' | term()``

get routing\_table's checksum.

create/0
~~~~~~~~

``create() -> {ok, Members, HashValues} | {error, any()}``

-  ``Members = [#member{}]``
-  ``HashValues = [{atom(), integer()}]``

Create the RING

create/1
~~~~~~~~

``create(Ver) -> {ok, Members, HashValues} | {error, any()}``

-  ``Ver = '?VER_CUR' | '?VER_PREV'``
-  ``Members = [#member{}]``
-  ``HashValues = [{atom(), integer()}]``

create/2
~~~~~~~~

``create(Ver, Members) -> {ok, Members, HashValues} | {error, any()}``

-  ``Ver = '?VER_CUR' | '?VER_PREV'``
-  ``Members = [#member{}]``
-  ``HashValues = [{atom(), integer()}]``

create/3
~~~~~~~~

``create(Ver, Members, Options) -> {ok, Members, HashValues} | {error, any()}``

-  ``Ver = '?VER_CUR' | '?VER_PREV'``
-  ``Members = [#member{}]``
-  ``Options = [{atom(), any()}]``
-  ``HashValues = [{atom(), integer()}]``

delete\_member\_by\_node/1
~~~~~~~~~~~~~~~~~~~~~~~~~~

``delete_member_by_node(Node) -> ok | {error, any()}``

-  ``Node = atom()``

remove a member by node-name.

detach/1
~~~~~~~~

``detach(Node) -> ok | {error, any()}``

-  ``Node = atom()``

detach a node.

detach/2
~~~~~~~~

``detach(Node, Clock) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``Clock = integer()``

dump/1
~~~~~~

``dump(Type) -> ok``

-  ``Type = member | ring | both | work``

Dump table-records.

force\_sync\_workers/0
~~~~~~~~~~~~~~~~~~~~~~

| ``force_sync_workers() -> ok``

Force sync ring-workers

get\_alias/2
~~~~~~~~~~~~

``get_alias(Node, GrpL2) -> {ok, tuple()}``

-  ``Node = atom()``
-  ``GrpL2 = string()``

Generate an alias of the node

get\_alias/3
~~~~~~~~~~~~

``get_alias(Table, Node, GrpL2) -> {ok, tuple()}``

-  ``Table = member_table()``
-  ``Node = atom()``
-  ``GrpL2 = string()``

get\_alias/4
~~~~~~~~~~~~

``get_alias(X1::init, Table, Node, GrpL2) -> {ok, tuple()}``

-  ``Table = member_table()``
-  ``Node = atom()``
-  ``GrpL2 = string()``

get\_cluster\_status/0
~~~~~~~~~~~~~~~~~~~~~~

| ``get_cluster_status() -> {ok, #'?CLUSTER_STAT'{}} | not_found``

Retrieve local cluster's status

get\_cluster\_tbl\_checksums/0
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| ``get_cluster_tbl_checksums() -> {ok, [tuple()]}``

Retrieve checksums of cluster-related tables

get\_member\_by\_node/1
~~~~~~~~~~~~~~~~~~~~~~~

``get_member_by_node(Node) -> {ok, #member{}} | {error, any()}``

-  ``Node = atom()``

get a member by node-name.

get\_members/0
~~~~~~~~~~~~~~

| ``get_members() -> {ok, [#member{}]} | {error, any()}``

get members.

get\_members/1
~~~~~~~~~~~~~~

| ``get_members(Ver::'?VER_CUR' | '?VER_PREV') -> {ok, list()} | {error, any()}``

get\_members\_by\_status/1
~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_members_by_status(Status) -> {ok, [#member{}]} | {error, any()}``

-  ``Status = atom()``

get members by status

get\_members\_by\_status/2
~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_members_by_status(Ver, Status) -> {ok, [#member{}]} | {error, any()}``

-  ``Ver = '?VER_CUR' | '?VER_PREV'``
-  ``Status = atom()``

get\_members\_count/0
~~~~~~~~~~~~~~~~~~~~~

| ``get_members_count() -> integer() | {error, any()}``

get # of members.

get\_options/0
~~~~~~~~~~~~~~

``get_options() -> {ok, Options}``

-  ``Options = [{atom(), any()}]``

get routing-table's options.

get\_redundancies\_by\_addr\_id/1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_redundancies_by_addr_id(AddrId) -> {ok, #redundancies{}} | {error, any()}``

-  ``AddrId = integer()``

Retrieve redundancies from the ring-table.

get\_redundancies\_by\_addr\_id/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_redundancies_by_addr_id(Method, AddrId) -> {ok, #redundancies{}} | {error, any()}``

-  ``Method = method()``
-  ``AddrId = integer()``

get\_redundancies\_by\_key/1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_redundancies_by_key(Key) -> {ok, #redundancies{}} | {error, any()}``

-  ``Key = binary()``

Retrieve redundancies from the ring-table.

get\_redundancies\_by\_key/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_redundancies_by_key(Method, Key) -> {ok, #redundancies{}} | {error, any()}``

-  ``Method = method()``
-  ``Key = binary()``

get\_remote\_clusters/0
~~~~~~~~~~~~~~~~~~~~~~~

| ``get_remote_clusters() -> {ok, [#'?CLUSTER_INFO'{}]} | {error, any()}``

Retrieve conf of remote clusters

get\_remote\_clusters/1
~~~~~~~~~~~~~~~~~~~~~~~

``get_remote_clusters(NumOfDestClusters) -> {ok, [#'?CLUSTER_INFO'{}]} | {error, any()}``

-  ``NumOfDestClusters = integer()``

get\_remote\_members/1
~~~~~~~~~~~~~~~~~~~~~~

``get_remote_members(ClusterId) -> {ok, #'?CLUSTER_MEMBER'{}} | {error, any()}``

-  ``ClusterId = atom()``

Retrieve remote cluster members

get\_remote\_members/2
~~~~~~~~~~~~~~~~~~~~~~

``get_remote_members(ClusterId, NumOfMembers) -> {ok, #'?CLUSTER_MEMBER'{}} | {error, any()}``

-  ``ClusterId = atom()``
-  ``NumOfMembers = integer()``

get\_ring/0
~~~~~~~~~~~

| ``get_ring() -> {ok, [tuple()]}``

Retrieve Ring

get\_ring/1
~~~~~~~~~~~

``get_ring(SyncTarget) -> {ok, [tuple()]}``

-  ``SyncTarget = sync_target()``

has\_charge\_of\_node/2
~~~~~~~~~~~~~~~~~~~~~~~

``has_charge_of_node(Key, NumOfReplicas) -> boolean()``

-  ``Key = binary()``
-  ``NumOfReplicas = integer()``

Has charge of node? 'true' is returned even if it detects an error

has\_member/1
~~~~~~~~~~~~~

``has_member(Node) -> boolean()``

-  ``Node = atom()``

Has a member ?

is\_alive/0
~~~~~~~~~~~

| ``is_alive() -> ok``

Is alive the process?

range\_of\_vnodes/1
~~~~~~~~~~~~~~~~~~~

``range_of_vnodes(ToVNodeId) -> {ok, [tuple()]}``

-  ``ToVNodeId = integer()``

Retrieve range of vnodes.

rebalance/0
~~~~~~~~~~~

| ``rebalance() -> {ok, [tuple()]} | {error, any()}``

Re-balance objects in the cluster.

reserve/3
~~~~~~~~~

``reserve(Node, CurState, Clock) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``CurState = atom()``
-  ``Clock = integer()``

reserve a node during in operation

reserve/5
~~~~~~~~~

``reserve(Node, CurState, AwarenessL2, Clock, NumOfVNodes) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``CurState = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``
-  ``NumOfVNodes = integer()``

reserve/6
~~~~~~~~~

``reserve(Node, CurState, AwarenessL2, Clock, NumOfVNodes, RPCPort) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``CurState = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``
-  ``NumOfVNodes = integer()``
-  ``RPCPort = integer()``

set\_options/1
~~~~~~~~~~~~~~

``set_options(Options) -> ok``

-  ``Options = [{atom(), any()}]``

set routing-table's options.

suspend/1
~~~~~~~~~

``suspend(Node) -> ok | {error, any()}``

-  ``Node = atom()``

suspend a node. (disable)

suspend/2
~~~~~~~~~

``suspend(Node, Clock) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``Clock = integer()``

synchronize/2
~~~~~~~~~~~~~

``synchronize(SyncTarget, SyncData) -> {ok, integer()} | {ok, [{atom(), any()}]} | {error, any()}``

-  ``SyncTarget = sync_target()``
-  ``SyncData = [{atom(), any()}]``

synchronize member-list and routing-table.

synchronize/3
~~~~~~~~~~~~~

``synchronize(SyncTarget, SyncData, Options) -> {ok, [{atom(), any()}]} | {error, any()}``

-  ``SyncTarget = sync_target()``
-  ``SyncData = [{atom(), any()}]``
-  ``Options = [{atom(), any()}]``

synchronize member-list and routing-table.

table\_info/1
~~~~~~~~~~~~~

``table_info(Ver) -> ring_table_info()``

-  ``Ver = '?VER_CUR' | '?VER_PREV'``

Retrieve table-info by version.

table\_info/1
~~~~~~~~~~~~~

``table_info(X1) -> any()``

update\_member/1
~~~~~~~~~~~~~~~~

``update_member(Member) -> ok | {error, any()}``

-  ``Member = #member{}``

update members.

update\_member\_by\_node/2
~~~~~~~~~~~~~~~~~~~~~~~~~~

| ``update_member_by_node(Node::atom(), State::atom()) -> ok | {error, any()}``

update a member by node-name.

update\_member\_by\_node/3
~~~~~~~~~~~~~~~~~~~~~~~~~~

| ``update_member_by_node(Node::atom(), Clock::integer(), State::atom()) -> ok | {error, any()}``

update\_members/1
~~~~~~~~~~~~~~~~~

``update_members(Members) -> ok | {error, any()}``

-  ``Members = [#member{}]``

update members.
