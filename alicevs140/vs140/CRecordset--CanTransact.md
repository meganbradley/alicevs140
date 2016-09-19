---
title: "CRecordset::CanTransact"
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
ms.assetid: 3d8285af-9e99-4fda-a154-511771702052
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::CanTransact
Determines whether the recordset allows transactions.  
  
## Syntax  
  
```  
  
BOOL CanTransact( ) const;  
```  
  
## Return Value  
 Nonzero if the recordset allows transactions; otherwise 0.  
  
## Remarks  
 For more information, see the article [Transaction (ODBC)](../vs140/Transaction--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::BeginTrans](../vs140/CDatabase--BeginTrans.md)   
 [CDatabase::CommitTrans](../vs140/CDatabase--CommitTrans.md)   
 [CDatabase::Rollback](../vs140/CDatabase--Rollback.md)