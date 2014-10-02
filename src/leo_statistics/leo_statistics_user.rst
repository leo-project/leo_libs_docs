leo\_statistics\_user
============================

-  `Description <#description>`__
-  `Function Index <#index>`__
-  `Function Details <#functions>`__

The SNMP manager's operation.

**Behaviours:** ```snmpm_user`` <snmpm_user.html>`__.

**References**

-  ```https://github.com/leo-project/leo_statistics/blob/master/src/leo_statistics_user.erl`` <https://github.com/leo-project/leo_statistics/blob/master/src/leo_statistics_user.erl>`__

Description
-----------

The SNMP manager's operation

Function Index
--------------

+-------------------------------------------+----+
| `handle\_agent/5 <#handle_agent-5>`__     |    |
+-------------------------------------------+----+
| `handle\_error/3 <#handle_error-3>`__     |    |
+-------------------------------------------+----+
| `handle\_inform/3 <#handle_inform-3>`__   |    |
+-------------------------------------------+----+
| `handle\_pdu/4 <#handle_pdu-4>`__         |    |
+-------------------------------------------+----+
| `handle\_report/3 <#handle_report-3>`__   |    |
+-------------------------------------------+----+
| `handle\_trap/3 <#handle_trap-3>`__       |    |
+-------------------------------------------+----+

Function Details
----------------

handle\_agent/5
~~~~~~~~~~~~~~~

``handle_agent(Addr, Port, Type, SnmpInfo, UserData) -> any()``

handle\_error/3
~~~~~~~~~~~~~~~

``handle_error(ReqId, Reason, UserData) -> any()``

handle\_inform/3
~~~~~~~~~~~~~~~~

``handle_inform(TargetName, SnmpInformInfo, UserData) -> any()``

handle\_pdu/4
~~~~~~~~~~~~~

``handle_pdu(TargetName, ReqId, SnmpPduInfo, UserData) -> any()``

handle\_report/3
~~~~~~~~~~~~~~~~

``handle_report(TargetName, SnmpReportInfo, UserData) -> any()``

handle\_trap/3
~~~~~~~~~~~~~~

``handle_trap(TargetName, SnmpTrapInfo, UserData) -> any()``
