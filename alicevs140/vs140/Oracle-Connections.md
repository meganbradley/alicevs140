---
title: "Oracle Connections"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d317e763-44aa-47c9-abe8-261d513d894f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Oracle Connections
When you configure either an Oracle ODBC DSN or an OLE DB connection, you must have the Oracle SQL*Net client-side components installed. SQL\*Net is the Oracle network transport layer. Most Oracle ODBC drivers, including the Microsoft driver and the Microsoft OLE DB Oracle provider map, call directly to this SQL\*Net layer.  
  
 After SQL*Net is configured, notice your SQL\*Net connection string. Typically, this consists of a specifier for the Oracle database server name and the network protocol type (such as TCP/IP and named pipes). Often, the SQL\*Net connection string is mapped to an alias. In this case, it is only necessary to note the alias. For information about how to configure SQL\*Net, contact your Oracle DBA, refer to the SQL\*Net documentation, or refer to your Oracle ODBC driver Help file for an example of a connection string.  
  
## See Also  
 [Creating Database Connections](../vs140/Creating-Database-Connections.md)