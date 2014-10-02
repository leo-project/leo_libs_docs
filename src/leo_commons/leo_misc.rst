leo\_misc
================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_misc is miscellaneous utilities.

**References**

-  ```https://github.com/leo-project/leo_commons/blob/master/src/leo_misc.erl`` <https://github.com/leo-project/leo_commons/blob/master/src/leo_misc.erl>`__

Description
-----------

leo\_misc is miscellaneous utilities

Function Index
--------------

+---------------------------------------------+------------------------------------------------------------------------------+
| `any\_to\_binary/1 <#any_to_binary-1>`__    | Convert value from any-type to binary.                                       |
+---------------------------------------------+------------------------------------------------------------------------------+
| `binary\_tokens/2 <#binary_tokens-2>`__     | Retrieve tokens from binary-data by delimiter-char.                          |
+---------------------------------------------+------------------------------------------------------------------------------+
| `get\_env/2 <#get_env-2>`__                 | Returns the value of the configuration parameter Par application from ETS.   |
+---------------------------------------------+------------------------------------------------------------------------------+
| `get\_env/3 <#get_env-3>`__                 | Returns the value of the configuration parameter Par application from ETS.   |
+---------------------------------------------+------------------------------------------------------------------------------+
| `get\_value/2 <#get_value-2>`__             | Retrieve a value from prop-lists.                                            |
+---------------------------------------------+------------------------------------------------------------------------------+
| `get\_value/3 <#get_value-3>`__             | Retrieve a value from prop-lists.                                            |
+---------------------------------------------+------------------------------------------------------------------------------+
| `init\_env/0 <#init_env-0>`__               | Initialize table of env.                                                     |
+---------------------------------------------+------------------------------------------------------------------------------+
| `node\_existence/1 <#node_existence-1>`__   | check a node existence.                                                      |
+---------------------------------------------+------------------------------------------------------------------------------+
| `node\_existence/2 <#node_existence-2>`__   | check a node existence.                                                      |
+---------------------------------------------+------------------------------------------------------------------------------+
| `set\_env/3 <#set_env-3>`__                 | Sets the value of the configuration parameter Par for Application to ETS.    |
+---------------------------------------------+------------------------------------------------------------------------------+

Function Details
----------------

any\_to\_binary/1
~~~~~~~~~~~~~~~~~

``any_to_binary(V) -> binary()``

-  ``V = binary()``

Convert value from any-type to binary

binary\_tokens/2
~~~~~~~~~~~~~~~~

``binary_tokens(Bin, Delimiter) -> Tokens::[binary]``

-  ``Bin = binary()``
-  ``Delimiter = binary()``

Retrieve tokens from binary-data by delimiter-char

get\_env/2
~~~~~~~~~~

``get_env(AppName, Key) -> {ok, any()} | undefined``

-  ``AppName = atom()``
-  ``Key = any()``

Returns the value of the configuration parameter Par application from
ETS

get\_env/3
~~~~~~~~~~

``get_env(AppName, Key, Default) -> {ok, any()} | undefined``

-  ``AppName = atom()``
-  ``Key = any()``
-  ``Default = any()``

Returns the value of the configuration parameter Par application from
ETS

get\_value/2
~~~~~~~~~~~~

``get_value(Key, Props) -> undefined | any()``

-  ``Key = any()``
-  ``Props = [tuple()]``

Retrieve a value from prop-lists

get\_value/3
~~~~~~~~~~~~

``get_value(Key, Props, Default) -> undefined | any()``

-  ``Key = any()``
-  ``Props = [tuple()]``
-  ``Default = any()``

Retrieve a value from prop-lists

init\_env/0
~~~~~~~~~~~

| ``init_env() -> ok``

Initialize table of env

node\_existence/1
~~~~~~~~~~~~~~~~~

``node_existence(Node) -> Existence::boolean()``

-  ``Node = atom()``

check a node existence.

node\_existence/2
~~~~~~~~~~~~~~~~~

``node_existence(Node, Timeout) -> Existence::boolean()``

-  ``Node = atom()``
-  ``Timeout = pos_integer()``

check a node existence.

set\_env/3
~~~~~~~~~~

``set_env(AppName, Key, Val) -> ok``

-  ``AppName = atom()``
-  ``Key = any()``
-  ``Val = any()``

Sets the value of the configuration parameter Par for Application to ETS
