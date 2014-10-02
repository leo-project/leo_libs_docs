leo\_s3\_user\_credential
================================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The s3-user's credential record handler.

**References**

-  https://github.com/leo-project/leo\_s3\_libs/blob/master/src/leo\_s3\_user\_credential.erl

Description
-----------

The s3-user's credential record handler

Function Index
--------------

+----------------------------------------------------------------------+------------------------------------------------------------+
| `bulk\_put/1 <#bulk_put-1>`__                                        | Add buckets.                                               |
+----------------------------------------------------------------------+------------------------------------------------------------+
| `checksum/0 <#checksum-0>`__                                         | Retrieve checksum of the table.                            |
+----------------------------------------------------------------------+------------------------------------------------------------+
| `create\_table/2 <#create_table-2>`__                                | Create user-credential table(mnesia).                      |
+----------------------------------------------------------------------+------------------------------------------------------------+
| `delete/1 <#delete-1>`__                                             | Remote a credential-user info.                             |
+----------------------------------------------------------------------+------------------------------------------------------------+
| `find\_all/0 <#find_all-0>`__                                        | Retrieve all records.                                      |
+----------------------------------------------------------------------+------------------------------------------------------------+
| `find\_all\_with\_role/0 <#find_all_with_role-0>`__                  | Retrieve all records with role.                            |
+----------------------------------------------------------------------+------------------------------------------------------------+
| `find\_by\_access\_key\_id/1 <#find_by_access_key_id-1>`__           | Retrieve a use by access-key-id.                           |
+----------------------------------------------------------------------+------------------------------------------------------------+
| `get\_credential\_by\_user\_id/1 <#get_credential_by_user_id-1>`__   | Retrieve credential by user-id.                            |
+----------------------------------------------------------------------+------------------------------------------------------------+
| `put/1 <#put-1>`__                                                   | Create a user account w/access-key-id/secret-access-key.   |
+----------------------------------------------------------------------+------------------------------------------------------------+
| `put/2 <#put-2>`__                                                   | Create a user account w/access-key-id/secret-access-key.   |
+----------------------------------------------------------------------+------------------------------------------------------------+

Function Details
----------------

bulk\_put/1
~~~~~~~~~~~

``bulk_put(UserCredentialList) -> ok``

-  ``UserCredentialList = [#user_credential{}]``

Add buckets

checksum/0
~~~~~~~~~~

| ``checksum() -> {ok, non_neg_integer()} | not_found | {error, any()}``

Retrieve checksum of the table

create\_table/2
~~~~~~~~~~~~~~~

``create_table(Mode, Nodes) -> ok``

-  ``Mode = ram_copies | disc_copies``
-  ``Nodes = list()``

Create user-credential table(mnesia)

delete/1
~~~~~~~~

``delete(UserId) -> ok | {error, any()}``

-  ``UserId = binary()``

Remote a credential-user info

find\_all/0
~~~~~~~~~~~

| ``find_all() -> {ok, [#user_credential{}]} | not_found | {error, any()}``

Retrieve all records

find\_all\_with\_role/0
~~~~~~~~~~~~~~~~~~~~~~~

| ``find_all_with_role() -> {ok, [#user_credential{}]} | not_found | {error, any()}``

Retrieve all records with role

find\_by\_access\_key\_id/1
~~~~~~~~~~~~~~~~~~~~~~~~~~~

``find_by_access_key_id(AccessKeyId) -> {ok, #user_credential{}} | not_found | {error, any()}``

-  ``AccessKeyId = binary()``

Retrieve a use by access-key-id

get\_credential\_by\_user\_id/1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``get_credential_by_user_id(UserId) -> {ok, [tuple()]} | not_found | {error, any()}``

-  ``UserId = binary()``

Retrieve credential by user-id

put/1
~~~~~

``put(UserCredential) -> ok | {ok, [tuple()]} | {error, any()}``

-  ``UserCredential = #user_credential{} | binary``

Create a user account w/access-key-id/secret-access-key

put/2
~~~~~

``put(UserId, CreatedAt) -> ok | {ok, [tuple()]} | {error, any()}``

-  ``UserId = binary()``
-  ``CreatedAt = non_neg_integer()``

Create a user account w/access-key-id/secret-access-key
