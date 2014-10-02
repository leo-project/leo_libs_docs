leo\_dcerl
=================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The disc cache API.

**References**

-  https://github.com/leo-project/leo\_dcerl/blob/master/src/leo\_dcerl.erl

Description
-----------

The disc cache API

Function Index
--------------

+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `delete/1 <#delete-1>`__                | Delete all of key-value pairs from the specified leo\_dcerl erlang process.                                    |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `get/2 <#get-2>`__                      | Get a value corresponding with the specified key from the specified leo\_dcerl erlang process.                 |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `get\_chunk/2 <#get_chunk-2>`__         | Get a chunk corresponding with the specified file descriptor from the specified leo\_dcerl erlang process.     |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `get\_filepath/2 <#get_filepath-2>`__   | Get a metadata AND status corresponding with the specified key from the specified leo\_dcerl erlang process.   |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `put/3 <#put-3>`__                      | Put a key-value pair into the specified leo\_dcerl erlang process.                                             |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `put\_begin/2 <#put_begin-2>`__         | Begin a transaction to put a large key-value pair into the specified leo\_dcerl erlang process.                |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `put\_chunk/3 <#put_chunk-3>`__         | Put a chunk into the specified leo\_dcerl erlang process while doing transaction.                              |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `put\_end/4 <#put_end-4>`__             | End a transaction to put a large key-value pair into the specified leo\_dcerl erlang process.                  |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `remove/2 <#remove-2>`__                | Remove a key-value pair from the specified leo\_dcerl erlang process.                                          |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `start/4 <#start-4>`__                  | Start a leo\_dcerl erlang process with specified settings.                                                     |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `stats/1 <#stats-1>`__                  | Get a status from the specified leo\_dcerl erlang process.                                                     |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                    | Stop the specified leo\_dcerl erlang process.                                                                  |
+-----------------------------------------+----------------------------------------------------------------------------------------------------------------+

Function Details
----------------

delete/1
~~~~~~~~

``delete(State) -> {ok, #dcerl_state{}} | {error, any()}``

-  ``State = #dcerl_state{}``

Delete all of key-value pairs from the specified leo\_dcerl erlang
process

get/2
~~~~~

``get(State, Key) -> {ok, #dcerl_state{}, binary()} | {ok, #dcerl_state{}, #dcerl_fd{}} | {error, any()}``

-  ``State = #dcerl_state{}``
-  ``Key = binary()``

Get a value corresponding with the specified key from the specified
leo\_dcerl erlang process

get\_chunk/2
~~~~~~~~~~~~

``get_chunk(State, Fd) -> {ok, #dcerl_state{}, #dcerl_fd{}, Chunk::binary(), Tail::boolean()} | {error, any()}``

-  ``State = #dcerl_state{}``
-  ``Fd = #dcerl_fd{}``

Get a chunk corresponding with the specified file descriptor from the
specified leo\_dcerl erlang process

get\_filepath/2
~~~~~~~~~~~~~~~

``get_filepath(State, Key) -> {ok, #dcerl_state{}, #cache_meta{}} | {error, any()}``

-  ``State = #dcerl_state{}``
-  ``Key = binary()``

Get a metadata AND status corresponding with the specified key from the
specified leo\_dcerl erlang process

put/3
~~~~~

``put(State, Key, Val) -> {ok, #dcerl_state{}} | {error, any()}``

-  ``State = #dcerl_state{}``
-  ``Key = binary()``
-  ``Val = binary()``

Put a key-value pair into the specified leo\_dcerl erlang process

put\_begin/2
~~~~~~~~~~~~

``put_begin(State, Key) -> {ok, #dcerl_state{}, #dcerl_fd{}} | {error, any()}``

-  ``State = #dcerl_state{}``
-  ``Key = binary()``

Begin a transaction to put a large key-value pair into the specified
leo\_dcerl erlang process

put\_chunk/3
~~~~~~~~~~~~

``put_chunk(State, Fd, Chunk) -> ok | {error, any()}``

-  ``State = #dcerl_state{}``
-  ``Fd = #dcerl_fd{}``
-  ``Chunk = binary()``

Put a chunk into the specified leo\_dcerl erlang process while doing
transaction

put\_end/4
~~~~~~~~~~

``put_end(State, Fd, CM, Commit) -> {ok, #dcerl_state{}} | {error, any()}``

-  ``State = #dcerl_state{}``
-  ``Fd = #dcerl_fd{}``
-  ``CM = #cache_meta{}``
-  ``Commit = boolean()``

End a transaction to put a large key-value pair into the specified
leo\_dcerl erlang process

remove/2
~~~~~~~~

``remove(State, Key) -> {ok, #dcerl_state{}} | {error, any()}``

-  ``State = #dcerl_state{}``
-  ``Key = binary()``

Remove a key-value pair from the specified leo\_dcerl erlang process

start/4
~~~~~~~

``start(DataDir, JournalDir, MaxSize, ChunkSize) -> {ok, #dcerl_state{}} | {error, any()}``

-  ``DataDir = string()``
-  ``JournalDir = string()``
-  ``MaxSize = integer()``
-  ``ChunkSize = integer()``

Start a leo\_dcerl erlang process with specified settings

stats/1
~~~~~~~

``stats(State) -> {ok, #cache_stats{}}``

-  ``State = #dcerl_state{}``

Get a status from the specified leo\_dcerl erlang process

stop/1
~~~~~~

``stop(State) -> {ok, #dcerl_state{}} | {error, any()}``

-  ``State = #dcerl_state{}``

Stop the specified leo\_dcerl erlang process
