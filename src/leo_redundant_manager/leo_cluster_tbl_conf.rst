leo\_cluster\_tbl\_conf
==============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The cluster conf table's operation.

**References**

-  https://github.com/leo-project/leo\_redundant\_manager/blob/master/src/leo\_cluster\_tbl\_conf.erl

Description
-----------

The cluster conf table's operation

Function Index
--------------

+-----------------------------------------+--------------------------------------------------+
| `all/0 <#all-0>`__                      | Retrieve all configuration of remote-clusters.   |
+-----------------------------------------+--------------------------------------------------+
| `checksum/0 <#checksum-0>`__            | Retrieve a checksum by cluster-id.               |
+-----------------------------------------+--------------------------------------------------+
| `create\_table/2 <#create_table-2>`__   | Create the system-configutation table.           |
+-----------------------------------------+--------------------------------------------------+
| `delete/1 <#delete-1>`__                | Remove a system-configuration.                   |
+-----------------------------------------+--------------------------------------------------+
| `find\_by\_ver/1 <#find_by_ver-1>`__    | Retrieve a system configuration.                 |
+-----------------------------------------+--------------------------------------------------+
| `get/0 <#get-0>`__                      | Retrieve a system configuration (latest).        |
+-----------------------------------------+--------------------------------------------------+
| `synchronize/1 <#synchronize-1>`__      | Synchronize records.                             |
+-----------------------------------------+--------------------------------------------------+
| `transform/0 <#transform-0>`__          | Transform records.                               |
+-----------------------------------------+--------------------------------------------------+
| `update/1 <#update-1>`__                | Modify a system-configuration.                   |
+-----------------------------------------+--------------------------------------------------+

Function Details
----------------

all/0
~~~~~

| ``all() -> {ok, [#'?SYSTEM_CONF'{}]} | not_found | {error, any()}``

Retrieve all configuration of remote-clusters

checksum/0
~~~~~~~~~~

| ``checksum() -> {ok, pos_integer()} | {error, any()}``

Retrieve a checksum by cluster-id

create\_table/2
~~~~~~~~~~~~~~~

``create_table(Mode, Nodes) -> ok | {error, any()}``

-  ``Mode = mnesia_copies()``
-  ``Nodes = [atom()]``

Create the system-configutation table

delete/1
~~~~~~~~

``delete(SystemConfig) -> ok | {error, any()}``

-  ``SystemConfig = #'?SYSTEM_CONF'{}``

Remove a system-configuration

find\_by\_ver/1
~~~~~~~~~~~~~~~

``find_by_ver(Ver) -> {ok, #'?SYSTEM_CONF'{}} | not_found | {error, any()}``

-  ``Ver = pos_integer()``

Retrieve a system configuration

get/0
~~~~~

| ``get() -> {ok, #'?SYSTEM_CONF'{}} | not_found | {error, any()}``

Retrieve a system configuration (latest)

synchronize/1
~~~~~~~~~~~~~

``synchronize(ValL) -> ok | {error, any()}``

-  ``ValL = [#'?SYSTEM_CONF'{}]``

Synchronize records

transform/0
~~~~~~~~~~~

| ``transform() -> ok | {error, any()}``

Transform records

update/1
~~~~~~~~

``update(SystemConfig) -> ok | {error, any()}``

-  ``SystemConfig = #'?SYSTEM_CONF'{}``

Modify a system-configuration
