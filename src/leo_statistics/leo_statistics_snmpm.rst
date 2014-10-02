leo\_statistics\_snmpm
=============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The SNMP manager.

**References**

-  https://github.com/leo-project/leo\_statistics/blob/master/src/leo\_statistics\_snmpm.erl

Description
-----------

The SNMP manager

Function Index
--------------

+--------------------------+------------------------------+
| `start/1 <#start-1>`__   | Start the snmpm.             |
+--------------------------+------------------------------+
| `walk/4 <#walk-4>`__     | Retrieve value from SNMPA.   |
+--------------------------+------------------------------+

Function Details
----------------

start/1
~~~~~~~

``start(Node) -> ok``

-  ``Node = atom()``

Start the snmpm

walk/4
~~~~~~

``walk(Node, Address, Port, Oid) -> {ok, #snmpa_value{}}``

-  ``Node = atom()``
-  ``Address = string()``
-  ``Port = pos_integer()``
-  ``Oid = [non_neg_integer()]``

Retrieve value from SNMPA
