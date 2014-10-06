leo\_hashtable
=====================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_hashtable is utilities for storing value as key-value in memory.

**References**

-  https://github.com/leo-project/leo\_commons/blob/master/src/leo\_hashtable.erl

Description
-----------

leo\_hashtable is utilities for storing value as key-value in memory

Function Index
--------------

+------------------------------+-------------------------------------+
| `all/1 <#all-1>`__           | Retrieve all values.                |
+------------------------------+-------------------------------------+
| `append/3 <#append-3>`__     | Append a value.                     |
+------------------------------+-------------------------------------+
| `clear/1 <#clear-1>`__       | Clear values into the hash-table.   |
+------------------------------+-------------------------------------+
| `delete/2 <#delete-2>`__     | Remove a value.                     |
+------------------------------+-------------------------------------+
| `destroy/1 <#destroy-1>`__   | Destroy an instance.                |
+------------------------------+-------------------------------------+
| `get/2 <#get-2>`__           | Retrieve a value by key.            |
+------------------------------+-------------------------------------+
| `get/3 <#get-3>`__           | Retrieve a value by key.            |
+------------------------------+-------------------------------------+
| `incr/2 <#incr-2>`__         | Increment a value.                  |
+------------------------------+-------------------------------------+
| `keys/1 <#keys-1>`__         | Retrieve all keys.                  |
+------------------------------+-------------------------------------+
| `new/0 <#new-0>`__           | Create an instance.                 |
+------------------------------+-------------------------------------+
| `new/1 <#new-1>`__           | Create an instance.                 |
+------------------------------+-------------------------------------+
| `put/3 <#put-3>`__           | Insert a value.                     |
+------------------------------+-------------------------------------+

Function Details
----------------

all/1
~~~~~

``all(Hashtable) -> [any()]``

-  ``Hashtable = pid()``

Retrieve all values

append/3
~~~~~~~~

``append(Hashtable, K, V) -> ok | {error, any()}``

-  ``Hashtable = pid()``
-  ``K = any()``
-  ``V = any()``

Append a value

clear/1
~~~~~~~

``clear(Hashtable) -> ok``

-  ``Hashtable = pid()``

Clear values into the hash-table

delete/2
~~~~~~~~

``delete(Hashtable, K) -> ok``

-  ``Hashtable = pid()``
-  ``K = any()``

Remove a value

destroy/1
~~~~~~~~~

``destroy(Hashtable) -> true``

-  ``Hashtable = pid()``

Destroy an instance

get/2
~~~~~

``get(Hashtable, K) -> any()``

-  ``Hashtable = pid()``
-  ``K = any()``

Retrieve a value by key

get/3
~~~~~

``get(Hashtable, K, DefaultValue) -> any()``

-  ``Hashtable = pid()``
-  ``K = any()``
-  ``DefaultValue = any()``

Retrieve a value by key

incr/2
~~~~~~

``incr(Hashtable, K) -> any()``

-  ``Hashtable = pid()``
-  ``K = any()``

Increment a value

keys/1
~~~~~~

``keys(Hashtable) -> list()``

-  ``Hashtable = pid()``

Retrieve all keys

new/0
~~~~~

| ``new() -> pid() | {error, any()}``

Create an instance

new/1
~~~~~

| ``new(X1::immutable) -> pid() | {error, any()}``

Create an instance

put/3
~~~~~

``put(Hashtable, K, V) -> ok``

-  ``Hashtable = pid()``
-  ``K = any()``
-  ``V = any()``

Insert a value
