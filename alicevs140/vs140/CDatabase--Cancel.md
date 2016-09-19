---
title: "CDatabase::Cancel"
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
ms.assetid: 24013ba7-f4a3-4af0-8d5c-e6d35b92bf10
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::Cancel
Call this member function to request that the data source cancel either an asynchronous operation in progress or a process from a second thread.  
  
## Syntax  
  
```  
  
void Cancel( );  
```  
  
## Remarks  
 Note that the MFC ODBC classes no longer use asynchronous processing; to perform an asychronous operation, you must directly call the ODBC API function [SQLSetConnectOption](https://msdn.microsoft.com/en-us/library/ms713564.aspx). For more information, see [Asynchronous Execution](https://msdn.microsoft.com/en-us/library/ms713563.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)