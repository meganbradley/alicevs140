---
title: "CRecordset::CanAppend"
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
ms.assetid: 4c055286-dd80-4088-9e22-8872c0fafa2e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::CanAppend
Determines whether the previously opened recordset allows you to add new records.  
  
## Syntax  
  
```  
  
BOOL CanAppend( ) const;  
```  
  
## Return Value  
 Nonzero if the recordset allows adding new records; otherwise 0. `CanAppend` will return 0 if you opened the recordset as read-only.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::AddNew](../vs140/CRecordset--AddNew.md)   
 [CRecordset::Requery](../vs140/CRecordset--Requery.md)