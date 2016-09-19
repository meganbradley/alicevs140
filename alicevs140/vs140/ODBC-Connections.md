---
title: "ODBC Connections"
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
ms.assetid: c9df2fa6-d9e2-4335-b885-724662968691
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ODBC Connections
ODBC connections are configured in the system Control Panel. ODBC connections can be made against any data source for which an ODBC driver has been installed. Visual C++ 6.0 or later ships drivers for text files, Access, FoxPro, Paradox, dBASE, Excel, SQL Server, and Oracle. When you create an ODBC connection, it automatically receives a data source name (DSN). The DSN is subsequently used to identify connections in data controls, such as ADO data control and RDO RemoteData control.  
  
 **OLE DB Connections** No additional work is necessary to configure an OLE DB connection. For example, if an ODBC data source is created, the OLE DB provider for ODBC automatically detects it.  
  
### To configure an ODBC data source  
  
1.  Click **Start**, click **Settings**, and then click **Control Panel**.  
  
2.  In Control Panel, select 32bit ODBC (Windows 95 or 98) or ODBC (Windows NT or 2000).  
  
3.  Click the **User DSN** or **System DSN** tab. **User DSN** lets you create user-specific data source names and **System DSN** lets you create data sources available to all users.  
  
4.  Click **Add** to display a list of locally installed ODBC drivers.  
  
5.  Select the driver corresponding to the type of indexed sequential access method (ISAM) or database you want to connect to, and then click **Finish**.  
  
6.  Follow the instructions specific to the driver. After closing, the DSN is available for use.  
  
 When generating a DSN for some ODBC driver types, you need to know the location of the actual file. For example when creating an Access DSN, you need to know the location of the .mdb file. Also, you should have a valid user name and password. For example, the system user name for most Access systems is *admin*.  
  
 When creating an [Oracle](../vs140/Oracle-Connections.md) DSN, you should know the SQL*Net connection string.  
  
## See Also  
 [Creating Database Connections](../vs140/Creating-Database-Connections.md)