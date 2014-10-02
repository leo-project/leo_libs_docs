leo\_s3\_user
====================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The s3-user operation.

**References**

-  https://github.com/leo-project/leo\_s3\_libs/blob/master/src/leo\_s3\_user.erl

Description
-----------

The s3-user operation

Function Index
--------------

+-----------------------------------------+---------------------------------------+
| `auth/2 <#auth-2>`__                    | Retrieve owners (omit secret\_key).   |
+-----------------------------------------+---------------------------------------+
| `bulk\_put/1 <#bulk_put-1>`__           | Add buckets.                          |
+-----------------------------------------+---------------------------------------+
| `checksum/0 <#checksum-0>`__            | Retrieve checksum of the table.       |
+-----------------------------------------+---------------------------------------+
| `create\_table/2 <#create_table-2>`__   | Create user table(mnesia).            |
+-----------------------------------------+---------------------------------------+
| `delete/1 <#delete-1>`__                | Delete a user.                        |
+-----------------------------------------+---------------------------------------+
| `find\_all/0 <#find_all-0>`__           | Retrieve all records.                 |
+-----------------------------------------+---------------------------------------+
| `find\_by\_id/1 <#find_by_id-1>`__      | Retrieve a user by user-id.           |
+-----------------------------------------+---------------------------------------+
| `put/1 <#put-1>`__                      | Insert a user.                        |
+-----------------------------------------+---------------------------------------+
| `put/3 <#put-3>`__                      | Create a user account.                |
+-----------------------------------------+---------------------------------------+
| `transform/0 <#transform-0>`__          | Transform data.                       |
+-----------------------------------------+---------------------------------------+
| `update/1 <#update-1>`__                | Update a user.                        |
+-----------------------------------------+---------------------------------------+

Function Details
----------------

auth/2
~~~~~~

``auth(UserId, Passwd) -> {ok, #'?S3_USER'{}} | {error, invalid_values}``

-  ``UserId = binary()``
-  ``Passwd = binary()``

Retrieve owners (omit secret\_key)

bulk\_put/1
~~~~~~~~~~~

``bulk_put(UserList) -> ok``

-  ``UserList = [#'?S3_USER'{}]``

Add buckets

checksum/0
~~~~~~~~~~

| ``checksum() -> {ok, non_neg_integer()} | not_found | {error, any()}``

Retrieve checksum of the table

create\_table/2
~~~~~~~~~~~~~~~

``create_table(Mode, Nodes) -> ok``

-  ``Mode = ram_copies | disc_copies``
-  ``Nodes = [atom()]``

Create user table(mnesia)

delete/1
~~~~~~~~

``delete(UserId) -> ok | {error, any()}``

-  ``UserId = binary()``

Delete a user

find\_all/0
~~~~~~~~~~~

| ``find_all() -> {ok, [#'?S3_USER'{}]} | not_found | {error, any()}``

Retrieve all records

find\_by\_id/1
~~~~~~~~~~~~~~

``find_by_id(UserId) -> {ok, #'?S3_USER'{}} | not_found | {error, any()}``

-  ``UserId = binary()``

Retrieve a user by user-id

put/1
~~~~~

``put(User) -> ok | {error, any()}``

-  ``User = #'?S3_USER'{}``

Insert a user

put/3
~~~~~

``put(UserId, Password, WithS3Keys) -> ok | {ok, [tuple()]} | {error, any()}``

-  ``UserId = binary()``
-  ``Password = binary()``
-  ``WithS3Keys = boolean()``

Create a user account

transform/0
~~~~~~~~~~~

| ``transform() -> ok``

Transform data

update/1
~~~~~~~~

``update(User) -> ok | {error, any()}``

-  ``User = #'?S3_USER'{}``

Update a user
