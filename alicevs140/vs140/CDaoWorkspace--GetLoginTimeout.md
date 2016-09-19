---
title: "CDaoWorkspace::GetLoginTimeout"
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
ms.topic: reference
ms.assetid: 1265d979-2066-4143-9c15-96561f95600d
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::GetLoginTimeout
Call this member function to get the current value of the DAO LoginTimeout property for the workspace.  
  
## Syntax  
  
```  
  
static short PASCAL GetLoginTimeout( );  
  
```  
  
## Return Value  
 The number of seconds before an error occurs when you attempt to log in to an ODBC database.  
  
## Remarks  
 This value represents the number of seconds before an error occurs when you attempt to log in to an ODBC database. The default LoginTimeout setting is 20 seconds. When LoginTimeout is set to 0, no timeout occurs and the communication with the data source might stop responding.  
  
 When you are attempting to log in to an ODBC database, such as Microsoft SQL Server, the connection may fail as a result of network errors or because the server is not running. Rather than waiting for the default 20 seconds to connect, you can specify how long the database engine waits before it produces an error. Logging in to the server happens implicitly as part of a number of different events, such as running a query on an external server database.  
  
 For related information, see the topic "LoginTimeout Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoWorkspace::SetLoginTimeout](../vs140/CDaoWorkspace--SetLoginTimeout.md)