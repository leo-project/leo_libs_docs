leo\_backend\_db\_server
===============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The gen\_server process for the process of database as part of a
supervision tree.

**Behaviours:** ```gen_server`` <gen_server.html>`__.

**References**

-  ```https://github.com/leo-project/leo_backend_db/blob/master/src/leo_backend_db_server.erl`` <https://github.com/leo-project/leo_backend_db/blob/master/src/leo_backend_db_server.erl>`__

Description
-----------

The gen\_server process for the process of database as part of a
supervision tree

Function Index
--------------

+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `close/1 <#close-1>`__                                   | Close the database.                                                           |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `code\_change/3 <#code_change-3>`__                      | Convert process state when code is changed.                                   |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `delete/2 <#delete-2>`__                                 | Delete an object from backend-db.                                             |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `fetch/4 <#fetch-4>`__                                   | Fetch records from backend-db.                                                |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `finish\_compaction/2 <#finish_compaction-2>`__          | Direct to end a compaction.                                                   |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `first/1 <#first-1>`__                                   | Retrieve a first record from backend-db.                                      |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `get/2 <#get-2>`__                                       | Retrieve an object from backend-db.                                           |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `get\_db\_raw\_filepath/1 <#get_db_raw_filepath-1>`__    | get database file path for calculating disk size.                             |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_call/3 <#handle_call-3>`__                      | gen\_server callback - Module:handle\_call(Request, From, State) -> Result.   |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_cast/2 <#handle_cast-2>`__                      | gen\_server callback - Module:handle\_cast(Request, State) -> Result.         |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `handle\_info/2 <#handle_info-2>`__                      | gen\_server callback - Module:handle\_info(Info, State) -> Result.            |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `init/1 <#init-1>`__                                     | gen\_server callback - Module:init(Args) -> Result.                           |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `put/3 <#put-3>`__                                       | Insert an object into backend-db.                                             |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `put\_value\_to\_new\_db/3 <#put_value_to_new_db-3>`__   | Direct to put a record to a temporary new data file.                          |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `run\_compaction/1 <#run_compaction-1>`__                | Direct to start a compaction.                                                 |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `start\_link/3 <#start_link-3>`__                        | Creates the gen\_server process as part of a supervision tree.                |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `status/1 <#status-1>`__                                 | Retrieve the current status from the database.                                |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `stop/1 <#stop-1>`__                                     | Close the process.                                                            |
+----------------------------------------------------------+-------------------------------------------------------------------------------+
| `terminate/2 <#terminate-2>`__                           | This function is called by a gen\_server when it is about to terminate.       |
+----------------------------------------------------------+-------------------------------------------------------------------------------+

Function Details
----------------

close/1
~~~~~~~

``close(Id) -> ok``

-  ``Id = atom()``

Close the database

code\_change/3
~~~~~~~~~~~~~~

``code_change(OldVsn, State, Extra) -> any()``

Convert process state when code is changed

gen\_server callback - Module:code\_change(OldVsn, State, Extra) -> {ok,
NewState} \| {error, Reason}.

delete/2
~~~~~~~~

| ``delete(Id::atom(), KeyBin::binary()) -> ok | {error, any()}``

Delete an object from backend-db.

fetch/4
~~~~~~~

``fetch(Id, KeyBin, Fun, MaxKeys) -> {ok, list()} | not_found | {error, any()}``

-  ``Id = atom()``
-  ``KeyBin = binary()``
-  ``Fun = function()``
-  ``MaxKeys = integer()``

Fetch records from backend-db.

finish\_compaction/2
~~~~~~~~~~~~~~~~~~~~

``finish_compaction(Id, Commit) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``Commit = boolean()``

Direct to end a compaction.

first/1
~~~~~~~

``first(Id) -> {ok, any(), any()} | {error, any()}``

-  ``Id = atom()``

Retrieve a first record from backend-db.

get/2
~~~~~

``get(Id, KeyBin) -> {ok, binary()} | not_found | {error, any()}``

-  ``Id = atom()``
-  ``KeyBin = binary()``

Retrieve an object from backend-db.

get\_db\_raw\_filepath/1
~~~~~~~~~~~~~~~~~~~~~~~~

``get_db_raw_filepath(Id) -> {ok, string()} | {error, any()}``

-  ``Id = atom()``

get database file path for calculating disk size.

handle\_call/3
~~~~~~~~~~~~~~

``handle_call(X1, From, State) -> any()``

gen\_server callback - Module:handle\_call(Request, From, State) ->
Result

handle\_cast/2
~~~~~~~~~~~~~~

``handle_cast(Msg, State) -> any()``

gen\_server callback - Module:handle\_cast(Request, State) -> Result

handle\_info/2
~~~~~~~~~~~~~~

``handle_info(Info, State) -> any()``

gen\_server callback - Module:handle\_info(Info, State) -> Result

init/1
~~~~~~

``init(X1) -> any()``

gen\_server callback - Module:init(Args) -> Result

put/3
~~~~~

``put(Id, KeyBin, ValueBin) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``KeyBin = binary()``
-  ``ValueBin = binary()``

Insert an object into backend-db.

put\_value\_to\_new\_db/3
~~~~~~~~~~~~~~~~~~~~~~~~~

``put_value_to_new_db(Id, KeyBin, ValueBin) -> ok | {error, any()}``

-  ``Id = atom()``
-  ``KeyBin = binary()``
-  ``ValueBin = binary()``

Direct to put a record to a temporary new data file.

run\_compaction/1
~~~~~~~~~~~~~~~~~

``run_compaction(Id) -> ok | {error, any()}``

-  ``Id = atom()``

Direct to start a compaction.

start\_link/3
~~~~~~~~~~~~~

``start_link(Id, DBModule, Path) -> {ok, pid()} | ignore | {error, any()}``

-  ``Id = atom()``
-  ``DBModule = atom()``
-  ``Path = string()``

Creates the gen\_server process as part of a supervision tree

status/1
~~~~~~~~

``status(Id) -> [{atom(), term()}]``

-  ``Id = atom()``

Retrieve the current status from the database

stop/1
~~~~~~

``stop(Id) -> any()``

Close the process

terminate/2
~~~~~~~~~~~

``terminate(Reason, State) -> any()``

This function is called by a gen\_server when it is about to terminate.
It should be the opposite of Module:init/1 and do any necessary cleaning
up. When it returns, the gen\_server terminates with Reason. The return
value is ignored.

gen\_server callback - Module:terminate(Reason, State)
