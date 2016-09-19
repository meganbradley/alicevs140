---
title: "Error: Transact-SQL execution ended without debugging"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - SQL
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7a4d4999-3973-4339-ba6a-f0d19bcb1d4a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error: Transact-SQL execution ended without debugging
This error occurs when you are trying to debug a Transact-SQL or SQLCLR procedure and the debugger does not receive debugging messages from the SQL Server.  
  
 This could be due to network problems or to problems on the SQL Server, but the most likely cause is a permissions problem.  
  
 There are two accounts involved:  
  
-   The application account is the user account that [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] is running as.  
  
-   The connection account is the identity used to make the connection to SQL Server. This is not necessarily the same as the identity that Visual Studio is running as if the connection is using SQL authentication.  
  
 SQL debugging requires that the application account must match the connection account or be sysadmin.  
  
 If you are using a SQL login like sa, the application account must be setup on the SQL Server as a sysadmin. By default, administrators on the machine SQL server is running on are SQL Server sysadmins.  
  
 To correct this error, you might need to:  
  
-   Verify your permissions settings. For more information, see [How to: Set SQL Server Permissions for Debugging](assetId:///84e088d0-0409-41d4-841b-f5d4b0fda414).  
  
-   Make sure SQL debugging if set up correctly.  
  
-   Consult with your network or database administrator.  
  
## See Also  
 [Setting Up SQL Debugging](assetId:///3db09e68-edcc-42de-9c22-4e97cfd55ab3)   
 [How to: Set SQL Server Permissions for Debugging](assetId:///84e088d0-0409-41d4-841b-f5d4b0fda414)   
 [Debug Settings and Preparation](../vs140/Debugger-Settings-and-Preparation.md)   
 [Remote Debugging Setup](../vs140/Remote-Debugging.md)