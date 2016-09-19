---
title: "CDatabase::CommitTrans"
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
ms.assetid: be4012df-5fae-4fcf-ac2b-cfbe2a6ba96d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::CommitTrans
Call this member function upon completing transactions.  
  
## Syntax  
  
```  
  
BOOL CommitTrans( );  
```  
  
## Return Value  
 Nonzero if the updates were successfully committed; otherwise 0. If **CommitTrans** fails, the state of the data source is undefined. You must check the data to determine its state.  
  
## Remarks  
 A transaction consists of a series of calls to the `AddNew`, **Edit**, **Delete**, and **Update** member functions of a `CRecordset` object that began with a call to the [BeginTrans](../vs140/CDatabase--BeginTrans.md) member function. **CommitTrans** commits the transaction. By default, updates are committed immediately; calling **BeginTrans** causes commitment of updates to be delayed until **CommitTrans** is called.  
  
 Until you call **CommitTrans** to end a transaction, you can call the [Rollback](../vs140/CDatabase--Rollback.md) member function to abort the transaction and leave the data source in its original state. To begin a new transaction, call **BeginTrans** again.  
  
 For more information about transactions, see the article [Transaction (ODBC)](../vs140/Transaction--ODBC-.md).  
  
## Example  
 See the article [Transaction: Performing a Transaction in a Recordset (ODBC)](../vs140/Transaction--Performing-a-Transaction-in-a-Recordset--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::BeginTrans](../vs140/CDatabase--BeginTrans.md)   
 [CDatabase::Rollback](../vs140/CDatabase--Rollback.md)