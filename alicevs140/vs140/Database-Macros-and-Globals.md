---
title: "Database Macros and Globals"
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
ms.assetid: 5b9b9e61-1cf9-4345-9f29-3807dd466488
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Database Macros and Globals
The macros and globals listed below apply to ODBC-based database applications. They are not used with DAO-based applications.  
  
 Before MFC 4.2, the macros `AFX_SQL_ASYNC` and `AFX_SQL_SYNC` gave asynchronous operations an opportunity to yield time to other processes. Beginning with MFC 4.2, the implementation of these macros changed because the MFC ODBC classes used only synchronous operations. The macro `AFX_ODBC_CALL` was new to MFC 4.2.  
  
### Database Macros  
  
|||  
|-|-|  
|[AFX_ODBC_CALL](../vs140/AFX_ODBC_CALL.md)|Calls an ODBC API function that returns `SQL_STILL_EXECUTING`. `AFX_ODBC_CALL` will repeatedly call the function until it no longer returns `SQL_STILL_EXECUTING`.|  
|[AFX_SQL_ASYNC](../vs140/AFX_SQL_ASYNC.md)|Calls `AFX_ODBC_CALL`.|  
|[AFX_SQL_SYNC](../vs140/AFX_SQL_SYNC.md)|Calls an ODBC API function that does not return `SQL_STILL_EXECUTING`.|  
  
### Database Globals  
  
|||  
|-|-|  
|[AfxGetHENV](../vs140/AfxGetHENV.md)|Retrieves a handle to the ODBC environment currently in use by MFC. You can use this handle in direct ODBC calls.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)