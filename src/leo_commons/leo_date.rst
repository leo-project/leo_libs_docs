leo\_date
================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_date is utilities for date processing.

**References**

-  ```https://github.com/leo-project/leo_commons/blob/master/src/leo_date.erl`` <https://github.com/leo-project/leo_commons/blob/master/src/leo_date.erl>`__

Description
-----------

leo\_date is utilities for date processing.

Function Index
--------------

+-------------------------------------------------------------------+--------------------------------------------------------+
| `clock/0 <#clock-0>`__                                            | Retrieve current time with unix-time.                  |
+-------------------------------------------------------------------+--------------------------------------------------------+
| `date\_format/0 <#date_format-0>`__                               | Format date.                                           |
+-------------------------------------------------------------------+--------------------------------------------------------+
| `date\_format/1 <#date_format-1>`__                               | Format date.                                           |
+-------------------------------------------------------------------+--------------------------------------------------------+
| `date\_format/2 <#date_format-2>`__                               | Format date.                                           |
+-------------------------------------------------------------------+--------------------------------------------------------+
| `greg\_seconds\_to\_unixtime/1 <#greg_seconds_to_unixtime-1>`__   | Convert data from a gregorian seconds to a unixtime.   |
+-------------------------------------------------------------------+--------------------------------------------------------+
| `now/0 <#now-0>`__                                                | Retrieve the current time.                             |
+-------------------------------------------------------------------+--------------------------------------------------------+
| `unixtime/0 <#unixtime-0>`__                                      | Retrieve unixtime.                                     |
+-------------------------------------------------------------------+--------------------------------------------------------+
| `unixtime\_to\_greg\_seconds/1 <#unixtime_to_greg_seconds-1>`__   | Convert data from a unixtime to a gregorian seconds.   |
+-------------------------------------------------------------------+--------------------------------------------------------+
| `zone/0 <#zone-0>`__                                              | Retrieve current timezone.                             |
+-------------------------------------------------------------------+--------------------------------------------------------+

Function Details
----------------

clock/0
~~~~~~~

| ``clock() -> integer()``

Retrieve current time with unix-time.

date\_format/0
~~~~~~~~~~~~~~

``date_format() -> any()``

Format date

date\_format/1
~~~~~~~~~~~~~~

``date_format(GregorianSeconds) -> string()``

-  ``GregorianSeconds = pos_integer()``

Format date

date\_format/2
~~~~~~~~~~~~~~

``date_format(Zone, GregorianSeconds) -> string()``

-  ``Zone = utc``
-  ``GregorianSeconds = pos_integer()``

Format date

greg\_seconds\_to\_unixtime/1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| ``greg_seconds_to_unixtime(GregorianSeconds::pos_integer()) -> pos_integer()``

Convert data from a gregorian seconds to a unixtime

now/0
~~~~~

| ``now() -> integer()``

Retrieve the current time. (the number of seconds from year 0 to now)

unixtime/0
~~~~~~~~~~

| ``unixtime() -> pos_integer()``

Retrieve unixtime

unixtime\_to\_greg\_seconds/1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``unixtime_to_greg_seconds(UnixTime) -> pos_integer()``

-  ``UnixTime = pos_integer()``

Convert data from a unixtime to a gregorian seconds

zone/0
~~~~~~

| ``zone() -> string()``

Retrieve current timezone
