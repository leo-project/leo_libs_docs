leo\_redundant\_manager\_worker
======================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The redundant manager's worker process.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  https://github.com/leo-project/leo\_redundant\_manager/blob/master/src/leo\_redundant\_manager\_worker.erl

Description
-----------

The redundant manager's worker process

Function Index
--------------

+----------------------------------------+-------------------------------------------------------------------------------+
| `checksum/0 <#checksum-0>`__           | Retrieve the checksums.                                                       |
+----------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__    | Convert process state when code is changed.                                   |
+----------------------------------------+-------------------------------------------------------------------------------+
| `dump/0 <#dump-0>`__                   | Dump the current ring-info.                                                   |
+----------------------------------------+-------------------------------------------------------------------------------+
| `first/1 <#first-1>`__                 | Retrieve the first record of the redundant-nodes.                             |
+----------------------------------------+-------------------------------------------------------------------------------+
| `force\_sync/1 <#force_sync-1>`__      | Force RING to synchronize with the manager-node.                              |
+----------------------------------------+-------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__    | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.   |
+----------------------------------------+-------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__    | Handling cast message.                                                        |
+----------------------------------------+-------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__    | Handling all non call/cast messages.                                          |
+----------------------------------------+-------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                   | Initiates the server.                                                         |
+----------------------------------------+-------------------------------------------------------------------------------+
| `last/1 <#last-1>`__                   | Retrieve the last record of the redundant-nodes.                              |
+----------------------------------------+-------------------------------------------------------------------------------+
| `lookup/2 <#lookup-2>`__               | Look up the redundant-nodes by address-id.                                    |
+----------------------------------------+-------------------------------------------------------------------------------+
| `redundancies/3 <#redundancies-3>`__   | Retrieve redundancies.                                                        |
+----------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/0 <#start_link-0>`__      | Start the server.                                                             |
+----------------------------------------+-------------------------------------------------------------------------------+
| `stop/0 <#stop-0>`__                   | Stop the server.                                                              |
+----------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__         | This function is called by a gen\_server when it is about to terminate.       |
+----------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

checksum/0
~~~~~~~~~~

``checksum() -> {ok, {PrevChecksum, CurChecksum}}``

-  ``PrevChecksum = integer()``
-  ``CurChecksum = integer()``

Retrieve the checksums

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

dump/0
~~~~~~

| ``dump() -> ok | {error, any()}``

Dump the current ring-info

first/1
~~~~~~~

``first(Table) -> {ok, #redundancies{}} | not_found``

-  ``Table = atom()``

Retrieve the first record of the redundant-nodes

force\_sync/1
~~~~~~~~~~~~~

``force_sync(Table) -> ok | {error, invalid_table}``

-  ``Table = atom()``

Force RING to synchronize with the manager-node

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(Handle, From, State) -> any()``

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

init/1
~~~~~~

``init(X1) -> any()``

Initiates the server

last/1
~~~~~~

``last(Table) -> {ok, #redundancies{}} | not_found``

-  ``Table = atom()``

Retrieve the last record of the redundant-nodes

lookup/2
~~~~~~~~

``lookup(Table, AddrId) -> {ok, #redundancies{}} | not_found``

-  ``Table = atom()``
-  ``AddrId = non_neg_integer()``

Look up the redundant-nodes by address-id

redundancies/3
~~~~~~~~~~~~~~

``redundancies(TableInfo, AddrId, Members) -> {ok, #redundancies{}} | not_found``

-  ``TableInfo = ring_table_info()``
-  ``AddrId = non_neg_integer()``
-  ``Members = [#member{}]``

Retrieve redundancies

start\_link/0
~~~~~~~~~~~~~

``start_link() -> any()``

Start the server

stop/0
~~~~~~

``stop() -> any()``

Stop the server

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason.
