leo\_object\_storage\_transformer
========================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The object storage's data transformer.

**References**

-  ```https://github.com/leo-project/leo_object_storage/blob/master/src/leo_object_storage_transformer.erl`` <https://github.com/leo-project/leo_object_storage/blob/master/src/leo_object_storage_transformer.erl>`__

Description
-----------

The object storage's data transformer

Function Index
--------------

+-----------------------------------------------------------------+------------------------------------------------+
| `cmeta\_bin\_into\_metadata/2 <#cmeta_bin_into_metadata-2>`__   | Set values from a custome-metadata.            |
+-----------------------------------------------------------------+------------------------------------------------+
| `header\_bin\_to\_metadata/1 <#header_bin_to_metadata-1>`__     | Transport a header-bin to a metadata.          |
+-----------------------------------------------------------------+------------------------------------------------+
| `list\_to\_cmeta\_bin/1 <#list_to_cmeta_bin-1>`__               | List to a custome-metadata(binary).            |
+-----------------------------------------------------------------+------------------------------------------------+
| `metadata\_to\_object/1 <#metadata_to_object-1>`__              | Transform from a metadata to an object.        |
+-----------------------------------------------------------------+------------------------------------------------+
| `object\_to\_metadata/1 <#object_to_metadata-1>`__              | Transfer object to metadata.                   |
+-----------------------------------------------------------------+------------------------------------------------+
| `transform\_metadata/1 <#transform_metadata-1>`__               | Transform old-type metadata to current-type.   |
+-----------------------------------------------------------------+------------------------------------------------+

Function Details
----------------

cmeta\_bin\_into\_metadata/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``cmeta_bin_into_metadata(CustomMetaBin, Metadata) -> #'?METADATA'{} | {error, any()}``

-  ``CustomMetaBin = binary()``
-  ``Metadata = #'?METADATA'{}``

Set values from a custome-metadata

header\_bin\_to\_metadata/1
~~~~~~~~~~~~~~~~~~~~~~~~~~~

``header_bin_to_metadata(HeaderBin) -> #'?METADATA'{} | {error, invaid_record}``

-  ``HeaderBin = binary()``

Transport a header-bin to a metadata

list\_to\_cmeta\_bin/1
~~~~~~~~~~~~~~~~~~~~~~

``list_to_cmeta_bin(CustomMeta) -> binary()``

-  ``CustomMeta = [{atom(), any()}]``

List to a custome-metadata(binary)

metadata\_to\_object/1
~~~~~~~~~~~~~~~~~~~~~~

``metadata_to_object(Metadata) -> #'?OBJECT'{} | {error, invaid_record}``

-  ``Metadata = #metadata{} | #'?METADATA'{}``

Transform from a metadata to an object

object\_to\_metadata/1
~~~~~~~~~~~~~~~~~~~~~~

``object_to_metadata(Object) -> #metadata_1{}``

-  ``Object = #object{} | #object_1{}``

Transfer object to metadata

transform\_metadata/1
~~~~~~~~~~~~~~~~~~~~~

``transform_metadata(Metadata) -> #metadata_1{} | {error, invaid_record}``

-  ``Metadata = #metadata{} | #metadata_1{}``

Transform old-type metadata to current-type
