leo\_s3\_auth
====================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The authentication API for S3-API.

**References**

-  https://github.com/leo-project/leo\_s3\_libs/blob/master/src/leo\_s3\_auth.erl

Description
-----------

The authentication API for S3-API

Function Index
--------------

+-------------------------------------------------+-------------------------------------------------+
| `authenticate/3 <#authenticate-3>`__            | Authenticate.                                   |
+-------------------------------------------------+-------------------------------------------------+
| `bulk\_put/1 <#bulk_put-1>`__                   | Add credentials.                                |
+-------------------------------------------------+-------------------------------------------------+
| `checksum/0 <#checksum-0>`__                    | Retrieve checksum of the table.                 |
+-------------------------------------------------+-------------------------------------------------+
| `create\_key/1 <#create_key-1>`__               | Generate access-key-id and secret-access-key.   |
+-------------------------------------------------+-------------------------------------------------+
| `create\_table/2 <#create_table-2>`__           | Create credential table(mnesia).                |
+-------------------------------------------------+-------------------------------------------------+
| `find\_all/0 <#find_all-0>`__                   | Retrieve all records.                           |
+-------------------------------------------------+-------------------------------------------------+
| `get\_credential/1 <#get_credential-1>`__       | Retrieve a credential from internal-db.         |
+-------------------------------------------------+-------------------------------------------------+
| `get\_signature/2 <#get_signature-2>`__         | Get AWS signature version 2.                    |
+-------------------------------------------------+-------------------------------------------------+
| `has\_credential/1 <#has_credential-1>`__       | Has a credential into the master-nodes?.        |
+-------------------------------------------------+-------------------------------------------------+
| `has\_credential/2 <#has_credential-2>`__       |                                                 |
+-------------------------------------------------+-------------------------------------------------+
| `put/1 <#put-1>`__                              | Add a credential (an authentication).           |
+-------------------------------------------------+-------------------------------------------------+
| `start/2 <#start-2>`__                          | Launch or create Mnesia/ETS.                    |
+-------------------------------------------------+-------------------------------------------------+
| `update\_providers/1 <#update_providers-1>`__   | update\_providers(slave only).                  |
+-------------------------------------------------+-------------------------------------------------+

Function Details
----------------

authenticate/3
~~~~~~~~~~~~~~

``authenticate(Authorization, SignParams, IsCreateBucketOp) -> {ok, binary()} | {error, any()}``

-  ``Authorization = binary()``
-  ``SignParams = #sign_params{}``
-  ``IsCreateBucketOp = boolean()``

Authenticate

bulk\_put/1
~~~~~~~~~~~

``bulk_put(CredentialList) -> ok``

-  ``CredentialList = [#credential{}]``

Add credentials

checksum/0
~~~~~~~~~~

| ``checksum() -> {ok, non_neg_integer()} | not_found | {error, any()}``

Retrieve checksum of the table

create\_key/1
~~~~~~~~~~~~~

``create_key(UserId) -> {ok, [tuple()]} | {error, any()}``

-  ``UserId = binary()``

Generate access-key-id and secret-access-key

create\_table/2
~~~~~~~~~~~~~~~

``create_table(Mode, Nodes) -> ok``

-  ``Mode = ram_copies | disc_copies``
-  ``Nodes = [atom()]``

Create credential table(mnesia)

find\_all/0
~~~~~~~~~~~

| ``find_all() -> {ok, [#credential{}]} | not_found | {error, any()}``

Retrieve all records

get\_credential/1
~~~~~~~~~~~~~~~~~

``get_credential(AccessKeyId) -> {ok, #credential{}} | not_found | {error, any()}``

-  ``AccessKeyId = binary()``

Retrieve a credential from internal-db

get\_signature/2
~~~~~~~~~~~~~~~~

``get_signature(SecretAccessKey, SignParams) -> binary()``

-  ``SecretAccessKey = binary()``
-  ``SignParams = #sign_params{}``

Get AWS signature version 2

has\_credential/1
~~~~~~~~~~~~~~~~~

``has_credential(AccessKeyId) -> boolean()``

-  ``AccessKeyId = binary()``

Has a credential into the master-nodes?

has\_credential/2
~~~~~~~~~~~~~~~~~

``has_credential(MasterNodes, AccessKey) -> boolean()``

-  ``MasterNodes = [atom()]``
-  ``AccessKey = binary()``

put/1
~~~~~

``put(Credential) -> ok | {error, any()}``

-  ``Credential = #credential{}``

Add a credential (an authentication)

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
