leo\_redundant\_manager
==============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_redaundant\_manager's server.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  https://github.com/leo-project/leo\_redundant\_manager/blob/master/src/leo\_redundant\_manager\_api.erl

Description
-----------

leo\_redaundant\_manager's server

Function Index
--------------

+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `attach/4 <#attach-4>`__                                    | Change node status to 'attach'.                                               |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `attach/5 <#attach-5>`__                                    |                                                                               |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `attach/6 <#attach-6>`__                                    |                                                                               |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `checksum/1 <#checksum-1>`__                                | Retrieve checksum of ring/member.                                             |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__                         | Convert process state when code is changed.                                   |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `create/1 <#create-1>`__                                    | Create the Rings.                                                             |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `delete\_member\_by\_node/1 <#delete_member_by_node-1>`__   | Remove a member by node.                                                      |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `detach/2 <#detach-2>`__                                    | Change node status to 'detach'.                                               |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `detach/3 <#detach-3>`__                                    |                                                                               |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `dump/1 <#dump-1>`__                                        | Dump files which are member and ring.                                         |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `get\_member\_by\_node/1 <#get_member_by_node-1>`__         | Retrieve a member by node.                                                    |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `get\_members/0 <#get_members-0>`__                         | Retrieve all members.                                                         |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `get\_members/1 <#get_members-1>`__                         |                                                                               |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `get\_members\_by\_status/2 <#get_members_by_status-2>`__   | Retrieve members by status.                                                   |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__                         | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.   |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__                         | Handling cast message.                                                        |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__                         | Handling all non call/cast messages.                                          |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `has\_member/1 <#has_member-1>`__                           | Is exists member?.                                                            |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                                        | Initiates the server.                                                         |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `reserve/5 <#reserve-5>`__                                  | Change node status to 'reserve'.                                              |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `reserve/6 <#reserve-6>`__                                  |                                                                               |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/0 <#start_link-0>`__                           | Start the process.                                                            |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `stop/0 <#stop-0>`__                                        | Stop the process.                                                             |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `suspend/2 <#suspend-2>`__                                  | Change node status to 'suspend'.                                              |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__                              | This function is called by a gen\_server when it is about to terminate.       |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `update\_member/1 <#update_member-1>`__                     | Modify a member.                                                              |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `update\_member\_by\_node/2 <#update_member_by_node-2>`__   | Modify a member by node.                                                      |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `update\_member\_by\_node/3 <#update_member_by_node-3>`__   |                                                                               |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+
| `update\_members/1 <#update_members-1>`__                   | Modify members.                                                               |
+-------------------------------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

attach/4
~~~~~~~~

``attach(Node, AwarenessL2, Clock, NumOfVNodes) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``
-  ``NumOfVNodes = integer()``

Change node status to 'attach'.

attach/5
~~~~~~~~

``attach(Node, AwarenessL2, Clock, NumOfVNodes, RPCPort) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``
-  ``NumOfVNodes = integer()``
-  ``RPCPort = integer()``

attach/6
~~~~~~~~

``attach(TableInfo, Node, AwarenessL2, Clock, NumOfVNodes, RPCPort) -> ok | {error, any()}``

-  ``TableInfo = ring_table_info()``
-  ``Node = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``
-  ``NumOfVNodes = integer()``
-  ``RPCPort = integer()``

checksum/1
~~~~~~~~~~

``checksum(Type) -> {ok, integer() | tuple()}``

-  ``Type = checksum_type()``

Retrieve checksum of ring/member

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

create/1
~~~~~~~~

``create(Ver) -> ok | {error, any()}``

-  ``Ver = '?VER_CUR' | '?VER_PREV'``

Create the Rings.

delete\_member\_by\_node/1
~~~~~~~~~~~~~~~~~~~~~~~~~~

``delete_member_by_node(Node) -> ok | {error, any()}``

-  ``Node = atom()``

Remove a member by node.

detach/2
~~~~~~~~

``detach(Node, Clock) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``Clock = integer()``

Change node status to 'detach'.

detach/3
~~~~~~~~

``detach(TableInfo, Node, Clock) -> ok | {error, any()}``

-  ``TableInfo = ring_table_info()``
-  ``Node = atom()``
-  ``Clock = integer()``

dump/1
~~~~~~

``dump(Type) -> ok``

-  ``Type = atom()``

Dump files which are member and ring.

get\_member\_by\_node/1
~~~~~~~~~~~~~~~~~~~~~~~

``get_member_by_node(Node) -> {ok, #member{}} | {error, any()}``

-  ``Node = atom()``

Retrieve a member by node.

get\_members/0
~~~~~~~~~~~~~~

| ``get_members() -> {ok, [#member{}]}``

Retrieve all members.

get\_members/1
~~~~~~~~~~~~~~

``get_members(Ver) -> {ok, [#member{}]}``

-  ``Ver = '?VER_CUR' | '?VER_PREV'``

get\_members\_by\_status/2
~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_members_by_status(Ver, Status) -> {ok, [#member{}]} | {error, any()}``

-  ``Ver = '?VER_CUR' | '?VER_PREV'``
-  ``Status = atom()``

Retrieve members by status.

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(X1, From, State) -> any()``

gen\_server callback - Module:handle\_call(Request, From, State) ->
Result

handle\_cast/2
~~~~~~~~~~~~~~

``handle_cast(Msg, State) -> any()``

Handling cast message

gen\_server callback - Module:handle\_cast(Request, State) -> Result.

handle\_info/2
~~~~~~~~~~~~~~

``handle_info(Info, State) -> any()``

Handling all non call/cast messages

gen\_server callback - Module:handle\_info(Info, State) -> Result.

has\_member/1
~~~~~~~~~~~~~

``has_member(Node) -> boolean()``

-  ``Node = atom()``

Is exists member?

init/1
~~~~~~

``init(X1) -> any()``

Initiates the server

reserve/5
~~~~~~~~~

``reserve(Node, CurState, AwarenessL2, Clock, NumOfVNodes) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``CurState = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``
-  ``NumOfVNodes = integer()``

Change node status to 'reserve'.

reserve/6
~~~~~~~~~

``reserve(Node, CurState, AwarenessL2, Clock, NumOfVNodes, RPCPort) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``CurState = atom()``
-  ``AwarenessL2 = string()``
-  ``Clock = integer()``
-  ``NumOfVNodes = integer()``
-  ``RPCPort = integer()``

start\_link/0
~~~~~~~~~~~~~

``start_link() -> any()``

Start the process

stop/0
~~~~~~

``stop() -> any()``

Stop the process

suspend/2
~~~~~~~~~

``suspend(Node, Clock) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``Clock = integer()``

Change node status to 'suspend'.

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason.

update\_member/1
~~~~~~~~~~~~~~~~

``update_member(Member) -> ok | {error, any()}``

-  ``Member = #member{}``

Modify a member.

update\_member\_by\_node/2
~~~~~~~~~~~~~~~~~~~~~~~~~~

``update_member_by_node(Node, NodeState) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``NodeState = atom()``

Modify a member by node.

update\_member\_by\_node/3
~~~~~~~~~~~~~~~~~~~~~~~~~~

``update_member_by_node(Node, Clock, NodeState) -> ok | {error, any()}``

-  ``Node = atom()``
-  ``Clock = integer()``
-  ``NodeState = atom()``

update\_members/1
~~~~~~~~~~~~~~~~~

``update_members(Members) -> ok | {error, any()}``

-  ``Members = [#member{}]``

Modify members.
