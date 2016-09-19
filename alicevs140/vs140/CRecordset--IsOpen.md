---
title: "CRecordset::IsOpen"
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
ms.assetid: 5c672129-2f5f-4711-952d-f81dfea7afb8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::IsOpen
Determines if the recordset is already open.  
  
## Syntax  
  
```  
  
BOOL IsOpen( ) const;  
```  
  
## Return Value  
 Nonzero if the recordset object's [Open](../vs140/CRecordset--Open.md) or [Requery](../vs140/CRecordset--Requery.md) member function has previously been called and the recordset has not been closed; otherwise 0.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)