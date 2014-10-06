leo\_file
================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

leo\_file is utilities for file processing.

**References**

-  https://github.com/leo-project/leo\_commons/blob/master/src/leo\_file.erl

Description
-----------

leo\_file is utilities for file processing

Function Index
--------------

+-----------------------------------------------------------+------------------------------------------------+
| `file\_delete\_all/1 <#file_delete_all-1>`__              | Remove all files of the target.                |
+-----------------------------------------------------------+------------------------------------------------+
| `file\_get\_mount\_path/1 <#file_get_mount_path-1>`__     | Retrieve file mount path(s).                   |
+-----------------------------------------------------------+------------------------------------------------+
| `file\_get\_remain\_disk/1 <#file_get_remain_disk-1>`__   | Retrieve remain disk capacity of the target.   |
+-----------------------------------------------------------+------------------------------------------------+
| `file\_get\_total\_size/1 <#file_get_total_size-1>`__     | Retrieve total of the file size.               |
+-----------------------------------------------------------+------------------------------------------------+
| `file\_touch/1 <#file_touch-1>`__                         | Touch a file.                                  |
+-----------------------------------------------------------+------------------------------------------------+
| `file\_unconsult/2 <#file_unconsult-2>`__                 | Unconsult the file.                            |
+-----------------------------------------------------------+------------------------------------------------+

Function Details
----------------

file\_delete\_all/1
~~~~~~~~~~~~~~~~~~~

``file_delete_all(FilePath) -> ok | {error, any()}``

-  ``FilePath = string()``

Remove all files of the target

file\_get\_mount\_path/1
~~~~~~~~~~~~~~~~~~~~~~~~

``file_get_mount_path(FilePath) -> ok | {error, any()}``

-  ``FilePath = string()``

Retrieve file mount path(s)

file\_get\_remain\_disk/1
~~~~~~~~~~~~~~~~~~~~~~~~~

``file_get_remain_disk(Params) -> ok | {error, any()}``

-  ``Params = {FilePath::string(), SizeKB::non_neg_integer(), Rate::non_neg_integer()}``

Retrieve remain disk capacity of the target

file\_get\_total\_size/1
~~~~~~~~~~~~~~~~~~~~~~~~

``file_get_total_size(Path) -> ok | {error, any()}``

-  ``Path = string()``

Retrieve total of the file size

file\_touch/1
~~~~~~~~~~~~~

``file_touch(FilePath) -> ok | {error, any}``

-  ``FilePath = string()``

Touch a file

file\_unconsult/2
~~~~~~~~~~~~~~~~~

``file_unconsult(FilePath, Term) -> ok | {error, any()}``

-  ``FilePath = string()``
-  ``Term = any()``

Unconsult the file
