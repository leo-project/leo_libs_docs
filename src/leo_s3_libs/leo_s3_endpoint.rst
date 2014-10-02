leo\_s3\_endpoint
========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The endpoint operation for S3-API.

**References**

-  https://github.com/leo-project/leo\_s3\_libs/blob/master/src/leo\_s3\_endpoint.erl

Description
-----------

The endpoint operation for S3-API

Function Index
--------------

+-------------------------------------------------+------------------------------------------------+
| `checksum/0 <#checksum-0>`__                    | Retrieve checksum of the table.                |
+-------------------------------------------------+------------------------------------------------+
| `create\_table/2 <#create_table-2>`__           | Create endpoint table(mnesia).                 |
+-------------------------------------------------+------------------------------------------------+
| `delete\_endpoint/1 <#delete_endpoint-1>`__     | Remove a End-Point from the Mnesia or ETS.     |
+-------------------------------------------------+------------------------------------------------+
| `get\_endpoints/0 <#get_endpoints-0>`__         | Retrieve a End-Point from the Mnesia or ETS.   |
+-------------------------------------------------+------------------------------------------------+
| `set\_endpoint/1 <#set_endpoint-1>`__           | Insert a End-Point into the Mnesia or ETS.     |
+-------------------------------------------------+------------------------------------------------+
| `start/2 <#start-2>`__                          | Launch or create Mnesia/ETS.                   |
+-------------------------------------------------+------------------------------------------------+
| `update\_providers/1 <#update_providers-1>`__   | update\_providers(slave only).                 |
+-------------------------------------------------+------------------------------------------------+

Function Details
----------------

checksum/0
~~~~~~~~~~

| ``checksum() -> {ok, non_neg_integer()} | not_found | {error, any()}``

Retrieve checksum of the table

create\_table/2
~~~~~~~~~~~~~~~

``create_table(Mode, Nodes) -> ok``

-  ``Mode = ram_copies | disc_copies``
-  ``Nodes = [atom()]``

Create endpoint table(mnesia)

delete\_endpoint/1
~~~~~~~~~~~~~~~~~~

``delete_endpoint(EndPoint) -> ok | {error, any()}``

-  ``EndPoint = binary()``

Remove a End-Point from the Mnesia or ETS

get\_endpoints/0
~~~~~~~~~~~~~~~~

| ``get_endpoints() -> {ok, [#endpoint{}]} | not_found | {error, any()}``

Retrieve a End-Point from the Mnesia or ETS

set\_endpoint/1
~~~~~~~~~~~~~~~

``set_endpoint(EndPoint) -> ok | not_found | {error, any()}``

-  ``EndPoint = binary()``

Insert a End-Point into the Mnesia or ETS

start/2
~~~~~~~

``start(Role, Providers) -> ok``

-  ``Role = master | slave``
-  ``Providers = [atom()]``

Launch or create Mnesia/ETS

update\_providers/1
~~~~~~~~~~~~~~~~~~~

``update_providers(Providers) -> ok``

-  ``Providers = [atom()]``

update\_providers(slave only)
