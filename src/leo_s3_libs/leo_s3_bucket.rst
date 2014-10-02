leo\_s3\_bucket
======================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The bucket operation for S3-API.

**References**

-  https://github.com/leo-project/leo\_s3\_libs/blob/master/src/leo\_s3\_bucket.erl

Description
-----------

The bucket operation for S3-API

Function Index
--------------

+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `aclinfo\_to\_str/1 <#aclinfo_to_str-1>`__                                   | Convert #bucket\_acl\_info to string to display ACL info on manager console.   |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `bulk\_put/1 <#bulk_put-1>`__                                                | Add buckets.                                                                   |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `change\_bucket\_owner/2 <#change_bucket_owner-2>`__                         | Is exist a bucket into the db.                                                 |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `checksum/0 <#checksum-0>`__                                                 | Retrieve checksum of the table.                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `create\_table/2 <#create_table-2>`__                                        |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `create\_table\_old\_for\_test/2 <#create_table_old_for_test-2>`__           |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `delete/2 <#delete-2>`__                                                     | delete a bucket.                                                               |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `delete/3 <#delete-3>`__                                                     |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `find\_all/0 <#find_all-0>`__                                                | Retrieve all buckets.                                                          |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `find\_all\_including\_owner/0 <#find_all_including_owner-0>`__              | Retrieve all buckets and owner.                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `find\_bucket\_by\_name/1 <#find_bucket_by_name-1>`__                        | Retrieve a bucket by bucket-name.                                              |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `find\_bucket\_by\_name/2 <#find_bucket_by_name-2>`__                        |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `find\_buckets\_by\_id/1 <#find_buckets_by_id-1>`__                          | Retrieve buckets by AccessKey.                                                 |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `find\_buckets\_by\_id/2 <#find_buckets_by_id-2>`__                          |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `get\_acls/1 <#get_acls-1>`__                                                | Retrive acls by a bucket.                                                      |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `head/2 <#head-2>`__                                                         | Is exist a bucket into the db.                                                 |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `head/4 <#head-4>`__                                                         |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `put/1 <#put-1>`__                                                           | put a bucket.                                                                  |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `put/2 <#put-2>`__                                                           |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `put/3 <#put-3>`__                                                           |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `put/4 <#put-4>`__                                                           |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `put/5 <#put-5>`__                                                           |                                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `start/3 <#start-3>`__                                                       | Launch a lib.                                                                  |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `transform/0 <#transform-0>`__                                               | The table schema migrate to the new one by using mnesia:transform\_table.      |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `transform/1 <#transform-1>`__                                               | Transform data.                                                                |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `update\_acls/3 <#update_acls-3>`__                                          | update acls in a bukcet-property.                                              |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `update\_acls2authenticated\_read/2 <#update_acls2authenticated_read-2>`__   | update acls to 'authenticated\_read'.                                          |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `update\_acls2private/2 <#update_acls2private-2>`__                          | update acls to 'private'.                                                      |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `update\_acls2public\_read/2 <#update_acls2public_read-2>`__                 | update acls to 'public\_read'.                                                 |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `update\_acls2public\_read\_write/2 <#update_acls2public_read_write-2>`__    | update acls to 'public\_read\_write'.                                          |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+
| `update\_providers/1 <#update_providers-1>`__                                | update\_providers(slave only).                                                 |
+------------------------------------------------------------------------------+--------------------------------------------------------------------------------+

Function Details
----------------

aclinfo\_to\_str/1
~~~~~~~~~~~~~~~~~~

``aclinfo_to_str(BucketACLInfoList) -> string()``

-  ``BucketACLInfoList = [#bucket_acl_info{}]``

Convert #bucket\_acl\_info to string to display ACL info on manager
console

bulk\_put/1
~~~~~~~~~~~

``bulk_put(BucketList) -> ok``

-  ``BucketList = [#'?BUCKET'{}]``

Add buckets

change\_bucket\_owner/2
~~~~~~~~~~~~~~~~~~~~~~~

``change_bucket_owner(AccessKey, Bucket) -> ok | not_found | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``

Is exist a bucket into the db

checksum/0
~~~~~~~~~~

| ``checksum() -> {ok, non_neg_integer()} | not_found | {error, any()}``

Retrieve checksum of the table

create\_table/2
~~~~~~~~~~~~~~~

``create_table(Mode, Nodes) -> ok``

-  ``Mode = ram_copies | disc | copies``
-  ``Nodes = [atom()]``

create\_table\_old\_for\_test/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``create_table_old_for_test(Mode, Nodes) -> ok``

-  ``Mode = ram_copies | disc | copies``
-  ``Nodes = [atom()]``

delete/2
~~~~~~~~

``delete(AccessKey, Bucket) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``

delete a bucket.

delete/3
~~~~~~~~

``delete(AccessKey, Bucket, DB) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``
-  ``DB = ets | mnesia | undefined``

find\_all/0
~~~~~~~~~~~

| ``find_all() -> {ok, [#'?BUCKET'{}]} | not_found | {error, any()}``

Retrieve all buckets

find\_all\_including\_owner/0
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| ``find_all_including_owner() -> {ok, list()} | not_found | {error, any()}``

Retrieve all buckets and owner

find\_bucket\_by\_name/1
~~~~~~~~~~~~~~~~~~~~~~~~

``find_bucket_by_name(Bucket) -> {ok, #'?BUCKET'{}} | not_found | {error, any()}``

-  ``Bucket = binary()``

Retrieve a bucket by bucket-name

find\_bucket\_by\_name/2
~~~~~~~~~~~~~~~~~~~~~~~~

``find_bucket_by_name(Bucket, LastModifiedAt) -> {ok, #'?BUCKET'{}} | {ok, match} | {error, any()}``

-  ``Bucket = binary()``
-  ``LastModifiedAt = non_neg_integer()``

find\_buckets\_by\_id/1
~~~~~~~~~~~~~~~~~~~~~~~

``find_buckets_by_id(AccessKey) -> {ok, [#'?BUCKET'{}]} | not_found | {error, any()}``

-  ``AccessKey = binary()``

Retrieve buckets by AccessKey

find\_buckets\_by\_id/2
~~~~~~~~~~~~~~~~~~~~~~~

``find_buckets_by_id(AccessKey, Checksum) -> {ok, [#'?BUCKET'{}]} | {ok, match} | not_found | {error, any()}``

-  ``AccessKey = binary()``
-  ``Checksum = non_neg_integer()``

get\_acls/1
~~~~~~~~~~~

``get_acls(Bucket) -> {ok, acls()} | not_found | {error, any()}``

-  ``Bucket = binary()``

Retrive acls by a bucket

head/2
~~~~~~

``head(AccessKey, Bucket) -> ok | not_found | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``

Is exist a bucket into the db

head/4
~~~~~~

``head(AccessKey, Bucket, DB, Providers) -> {ok, #'?BUCKET'{}} | not_found | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``
-  ``DB = atom()``
-  ``Providers = [atom()]``

put/1
~~~~~

``put(Bucket) -> ok | {error, any()}``

-  ``Bucket = #'?BUCKET'{}``

put a bucket.

put/2
~~~~~

``put(AccessKey, BucketName) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``BucketName = binary()``

put/3
~~~~~

``put(AccessKey, BucketName, CannedACL) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``BucketName = binary()``
-  ``CannedACL = string()``

put/4
~~~~~

``put(AccessKey, BucketName, CannedACL, ClusterId) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``BucketName = binary()``
-  ``CannedACL = string()``
-  ``ClusterId = atom()``

put/5
~~~~~

``put(AccessKey, BucketName, CannedACL, ClusterId, DB) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``BucketName = binary()``
-  ``CannedACL = string()``
-  ``ClusterId = atom()``
-  ``DB = ets | mnesia | undefined``

start/3
~~~~~~~

``start(Role, Provider, SyncInterval) -> ok``

-  ``Role = master | slave``
-  ``Provider = [atom()]``
-  ``SyncInterval = non_neg_integer()``

Launch a lib

transform/0
~~~~~~~~~~~

| ``transform() -> ok``

The table schema migrate to the new one by using mnesia:transform\_table

transform/1
~~~~~~~~~~~

``transform(ClusterId) -> any()``

Transform data

update\_acls/3
~~~~~~~~~~~~~~

``update_acls(AccessKey, Bucket, ACLs) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``
-  ``ACLs = acls()``

update acls in a bukcet-property

update\_acls2authenticated\_read/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``update_acls2authenticated_read(AccessKey, Bucket) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``

update acls to 'authenticated\_read'

update\_acls2private/2
~~~~~~~~~~~~~~~~~~~~~~

``update_acls2private(AccessKey, Bucket) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``

update acls to 'private'

update\_acls2public\_read/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~

``update_acls2public_read(AccessKey, Bucket) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``

update acls to 'public\_read'

update\_acls2public\_read\_write/2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``update_acls2public_read_write(AccessKey, Bucket) -> ok | {error, any()}``

-  ``AccessKey = binary()``
-  ``Bucket = binary()``

update acls to 'public\_read\_write'

update\_providers/1
~~~~~~~~~~~~~~~~~~~

``update_providers(Providers) -> ok``

-  ``Providers = [atom()]``

update\_providers(slave only)
