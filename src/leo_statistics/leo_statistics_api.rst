leo\_statistics\_api
===========================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The statistics API.

**References**

-  https://github.com/leo-project/leo\_statistics/blob/master/src/leo\_statistics\_api.erl

Description
-----------

The statistics API

Function Index
--------------

+-------------------------------------------+-----------------------------+
| `create\_tables/2 <#create_tables-2>`__   | Create the stat's tables.   |
+-------------------------------------------+-----------------------------+
| `start\_link/1 <#start_link-1>`__         | Start the SNMP server.      |
+-------------------------------------------+-----------------------------+

Function Details
----------------

create\_tables/2
~~~~~~~~~~~~~~~~

``create_tables(MnesiaDiscType, Nodes) -> ok``

-  ``MnesiaDiscType = disc_copies | ram_copies``
-  ``Nodes = [atom()]``

Create the stat's tables

start\_link/1
~~~~~~~~~~~~~

``start_link(Application) -> ok | {error, any()}``

-  ``Application = atom()``

Start the SNMP server
