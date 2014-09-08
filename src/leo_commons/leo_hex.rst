leo\_hex
===============

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_hex is utilities for calculation of hexadecimal.

Description
-----------

leo\_hex is utilities for calculation of hexadecimal

Function Index
--------------

+-------------------------------------------------------------+-------------------------------------------------+
| `binary\_to\_hex/1 <#binary_to_hex-1>`__                    | Convert the value from binary to hex.           |
+-------------------------------------------------------------+-------------------------------------------------+
| `hex\_to\_integer/1 <#hex_to_integer-1>`__                  | Convert the value from hex to integer.          |
+-------------------------------------------------------------+-------------------------------------------------+
| `hex\_to\_string/1 <#hex_to_string-1>`__                    | Convert the value from hex to string.           |
+-------------------------------------------------------------+-------------------------------------------------+
| `integer\_to\_hex/2 <#integer_to_hex-2>`__                  | Convert the value from integer to hex.          |
+-------------------------------------------------------------+-------------------------------------------------+
| `integer\_to\_raw\_binary/1 <#integer_to_raw_binary-1>`__   | Convert the value from integer to raw-binary.   |
+-------------------------------------------------------------+-------------------------------------------------+
| `integer\_to\_raw\_binary/2 <#integer_to_raw_binary-2>`__   | Convert the value from integer to raw-binary.   |
+-------------------------------------------------------------+-------------------------------------------------+
| `raw\_binary\_to\_integer/1 <#raw_binary_to_integer-1>`__   | Convert the value from binary to integer.       |
+-------------------------------------------------------------+-------------------------------------------------+

Function Details
----------------

binary\_to\_hex/1
~~~~~~~~~~~~~~~~~

``binary_to_hex(Bin) -> string()``

-  ``Bin = binary()``

Convert the value from binary to hex

hex\_to\_integer/1
~~~~~~~~~~~~~~~~~~

``hex_to_integer(Hex) -> integer()``

-  ``Hex = string()``

Convert the value from hex to integer

hex\_to\_string/1
~~~~~~~~~~~~~~~~~

``hex_to_string(Hex) -> string()``

-  ``Hex = string()``

Convert the value from hex to string

integer\_to\_hex/2
~~~~~~~~~~~~~~~~~~

``integer_to_hex(I, Len) -> string()``

-  ``I = integer()``
-  ``Len = pos_integer()``

Convert the value from integer to hex

integer\_to\_raw\_binary/1
~~~~~~~~~~~~~~~~~~~~~~~~~~

``integer_to_raw_binary(I) -> binary()``

-  ``I = integer()``

Convert the value from integer to raw-binary

integer\_to\_raw\_binary/2
~~~~~~~~~~~~~~~~~~~~~~~~~~

``integer_to_raw_binary(I, Len) -> binary()``

-  ``I = integer()``
-  ``Len = pos_integer()``

Convert the value from integer to raw-binary

raw\_binary\_to\_integer/1
~~~~~~~~~~~~~~~~~~~~~~~~~~

``raw_binary_to_integer(Bin) -> integer()``

-  ``Bin = binary()``

Convert the value from binary to integer
