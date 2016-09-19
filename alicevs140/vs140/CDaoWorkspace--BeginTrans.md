---
title: "CDaoWorkspace::BeginTrans"
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
ms.assetid: 9bb6acb5-7935-438c-b0e9-ccb6b06269bb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::BeginTrans
Call this member function to initiate a transaction.  
  
## Syntax  
  
```  
  
void BeginTrans( );  
  
```  
  
## Remarks  
 After you call **BeginTrans**, updates you make to your data or database structure take effect when you commit the transaction. Because the workspace defines a single transaction space, the transaction applies to all open databases in the workspace. There are two ways to complete the transaction:  
  
-   Call the [CommitTrans](../vs140/CDaoWorkspace--CommitTrans.md) member function to commit the transaction and save changes to the data source.  
  
-   Or call the [Rollback](../vs140/CDaoWorkspace--Rollback.md) member function to cancel the transaction.  
  
 Closing the workspace object or a database object while a transaction is pending rolls back all pending transactions.  
  
 If you need to isolate transactions on one ODBC data source from those on another ODBC data source, see the [SetIsolateODBCTrans](../vs140/CDaoWorkspace--SetIsolateODBCTrans.md) member function.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoWorkspace::GetIsolateODBCTrans](../vs140/CDaoWorkspace--GetIsolateODBCTrans.md)   
 [CDaoWorkspace::CommitTrans](../vs140/CDaoWorkspace--CommitTrans.md)   
 [CDaoWorkspace::Rollback](../vs140/CDaoWorkspace--Rollback.md)