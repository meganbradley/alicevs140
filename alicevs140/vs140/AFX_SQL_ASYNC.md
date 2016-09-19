---
title: "AFX_SQL_ASYNC"
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
ms.assetid: 161ae353-8b09-492d-aed7-dcd037d40963
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_SQL_ASYNC
The implementation of this macro changed in MFC 4.2.  
  
## Syntax  
  
```  
  
AFX_SQL_ASYNC(  
prs  
,   
SQLFunc )  
```  
  
#### Parameters  
 `prs`  
 A pointer to a `CRecordset` object or a `CDatabase` object. Beginning with MFC 4.2, this parameter value is ignored.  
  
 `SQLFunc`  
 An ODBC API function. For more information about ODBC API functions, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 `AFX_SQL_ASYNC` simply calls the macro [AFX_ODBC_CALL](../vs140/AFX_ODBC_CALL.md) and ignores the `prs` parameter. In versions of MFC prior to 4.2, `AFX_SQL_ASYNC` was used to call ODBC API functions that might return `SQL_STILL_EXECUTING`. If an ODBC API function did return `SQL_STILL_EXECUTING`, then `AFX_SQL_ASYNC` would call `prs->OnWaitForDataSource`.  
  
> [!NOTE]
>  The MFC ODBC classes now use only synchronous processing. In order to perform an asynchronous operation, you must call the ODBC API function **SQLSetConnectOption**. For more information, see the topic "Executing Functions Asynchronously" in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AFX_ODBC_CALL](../vs140/AFX_ODBC_CALL.md)   
 [AFX_SQL_SYNC](../vs140/AFX_SQL_SYNC.md)