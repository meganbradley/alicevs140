---
title: "AFX_ODBC_CALL"
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
ms.assetid: 9e5086bc-2ae2-45fa-b277-bfd14182fd1f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_ODBC_CALL
Use this macro to call any ODBC API function that may return `SQL_STILL_EXECUTING`.  
  
## Syntax  
  
```  
  
AFX_ODBC_CALL(  
SQLFunc )  
```  
  
#### Parameters  
 `SQLFunc`  
 An ODBC API function. For more information about ODBC API functions, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 `AFX_ODBC_CALL` repeatedly calls the function until it no longer returns `SQL_STILL_EXECUTING`.  
  
 Before invoking `AFX_ODBC_CALL`, you must declare a variable, `nRetCode`, of type **RETCODE**.  
  
 Note that the MFC ODBC classes now use only synchronous processing. In order to perform an asynchronous operation, you must call the ODBC API function **SQLSetConnectOption**. For more information, see the topic "Executing Functions Asynchronously" in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 This example uses `AFX_ODBC_CALL` to call the **SQLColumns** ODBC API function, which returns a list of the columns in the table named by `strTableName`. Note the declaration of `nRetCode` and the use of recordset data members to pass parameters to the function. The example also illustrates checking the results of the call with **Check**, a member function of class `CRecordset`. The variable `prs` is a pointer to a `CRecordset` object, declared elsewhere.  
  
 [!CODE [NVC_MFCDatabase#39](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#39)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AFX_SQL_ASYNC](../vs140/AFX_SQL_ASYNC.md)   
 [AFX_SQL_SYNC](../vs140/AFX_SQL_SYNC.md)