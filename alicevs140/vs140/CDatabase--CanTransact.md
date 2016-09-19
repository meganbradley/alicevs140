---
title: "CDatabase::CanTransact"
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
ms.assetid: 80996888-62ae-4fd5-8079-476beb719ddb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::CanTransact
Call this member function to determine whether the database allows transactions.  
  
## Syntax  
  
```  
  
BOOL CanTransact( ) const;  
```  
  
## Return Value  
 Nonzero if recordsets using this `CDatabase` object allow transactions; otherwise 0.  
  
## Remarks  
 For information about transactions, see the article [Transaction (ODBC)](../vs140/Transaction--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::BeginTrans](../vs140/CDatabase--BeginTrans.md)   
 [CDatabase::CommitTrans](../vs140/CDatabase--CommitTrans.md)   
 [CDatabase::Rollback](../vs140/CDatabase--Rollback.md)