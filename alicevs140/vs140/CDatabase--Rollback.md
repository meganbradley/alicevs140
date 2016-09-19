---
title: "CDatabase::Rollback"
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
ms.assetid: 42d03721-5e73-44ab-a2e3-b2fd9f049e16
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::Rollback
Call this member function to reverse the changes made during a transaction.  
  
## Syntax  
  
```  
  
BOOL Rollback( );  
```  
  
## Return Value  
 Nonzero if the transaction was successfully reversed; otherwise 0. If a **Rollback** call fails, the data source and transaction states are undefined. If **Rollback** returns 0, you must check the data source to determine its state.  
  
## Remarks  
 All `CRecordset` `AddNew`, **Edit**, **Delete**, and **Update** calls executed since the last [BeginTrans](../vs140/CDatabase--BeginTrans.md) are rolled back to the state that existed at the time of that call.  
  
 After a call to **Rollback**, the transaction is over, and you must call **BeginTrans** again for another transaction. The record that was current before you called **BeginTrans** becomes the current record again after **Rollback**.  
  
 After a rollback, the record that was current before the rollback remains current. For details about the state of the recordset and the data source after a rollback, see the article [Transaction (ODBC)](../vs140/Transaction--ODBC-.md).  
  
## Example  
 See the article [Transaction: Performing a Transaction in a Recordset (ODBC)](../vs140/Transaction--Performing-a-Transaction-in-a-Recordset--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::BeginTrans](../vs140/CDatabase--BeginTrans.md)   
 [CDatabase::CommitTrans](../vs140/CDatabase--CommitTrans.md)