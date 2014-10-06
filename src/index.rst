.. =========================================================
.. Leo Libs documentation
.. Copyright (c) 2012-2014 Rakuten, Inc.
.. http://leo-project.net/
.. =========================================================

Leo Libs Documentation
=======================

Data Storage and Cache
^^^^^^^^^^^^^^^^^^^^^^

* |leo_backend_db| is a wrapper library for Basho bitcask, Basho eleveldb and Erlang ETS. They are used as local KVS in LeoFS.
* |leo_cache| is an object caching server into RAM and Disc (SSD).
* |leo_dcerl| is a disc cache lib for Erlang.
* |leo_mcerl| is a memory cache lib for Erlang.
* |leo_object_storage| is a log-structured object/BLOB storage.

Distributed Computing
^^^^^^^^^^^^^^^^^^^^^

* |leo_ordning_reda| is a library to stack objects and send stacked objects with async.
* |leo_redundant_manager| manages a routing-table and monitors registered nodes in order to keep consistency of data.
* |leo_rpc| is an original rpc library, interface of which is similar to Erlang's RPC.

S3-API related
^^^^^^^^^^^^^^^^^^^^^^

* |leo_s3_libs| are S3-API related libraries for LeoFS and other Erlang applications.

Utilities
^^^^^^^^^^^^^^^^^^^^^^

* |leo_commons| includes common modules for LeoFS and other Erlang applications.
* |leo_logger| is a logging library for LeoFS and other Erlang applications. It has plugin-mechanism.
* |leo_mq| is a local message-queueing library.
* |leo_pod| is an Erlang worker pool manager. It is implemented no to use ETS (Erlang Term Storage)
* |leo_statistics| is a statistics library for LeoFS and other Erlang applications.

.. toctree::
   :hidden:

   leo_backend_db/leo_backend_db_toc
   leo_cache/leo_cache_toc
   leo_commons/leo_commons_toc
   leo_dcerl/leo_dcerl_toc
   leo_logger/leo_logger_toc
   leo_mcerl/leo_mcerl_toc
   leo_mq/leo_mq_toc
   leo_object_storage/leo_object_storage_toc
   leo_ordning_reda/leo_ordning_reda_toc
   leo_pod/leo_pod_toc
   leo_redundant_manager/leo_redundant_manager_toc
   leo_rpc/leo_rpc_toc
   leo_s3_libs/leo_s3_libs_toc
   leo_statistics/leo_statistics_toc



.. |leo_backend_db| raw:: html

   <a href="leo_backend_db/leo_backend_db_toc.html">leo_backend_db</a>

.. |leo_cache| raw:: html

   <a href="leo_cache/leo_cache_toc.html">leo_cache</a>

.. |leo_commons| raw:: html

   <a href="leo_commons/leo_commons_toc.html">leo_commons</a>

.. |leo_dcerl| raw:: html

   <a href="leo_dcerl/leo_dcerl_toc.html">leo_dcerl</a>

.. |leo_logger| raw:: html

   <a href="leo_logger/leo_logger_toc.html">leo_logger</a>

.. |leo_mcerl| raw:: html

   <a href="leo_mcerl/leo_mcerl_toc.html">leo_mcerl</a>

.. |leo_mq| raw:: html

   <a href="leo_mq/leo_mq_toc.html">leo_mq</a>

.. |leo_object_storage| raw:: html

   <a href="leo_object_storage/leo_object_storage_toc.html">leo_object_storage</a>

.. |leo_ordning_reda| raw:: html

   <a href="leo_ordning_reda/leo_ordning_reda_toc.html">leo_ordning_reda</a>

.. |leo_pod| raw:: html

   <a href="leo_pod/leo_pod_toc.html">leo_pod</a>

.. |leo_redundant_manager| raw:: html

   <a href="leo_redundant_manager/leo_redundant_manager_toc.html">leo_redundant_manager</a>

.. |leo_rpc| raw:: html

   <a href="leo_rpc/leo_rpc_toc.html">leo_rpc</a>

.. |leo_s3_libs| raw:: html

   <a href="leo_s3_libs/leo_s3_libs_toc.html">leo_s3_libs</a>

.. |leo_statistics| raw:: html

   <a href="leo_statistics/leo_statistics_toc.html">leo_statistics</a>
