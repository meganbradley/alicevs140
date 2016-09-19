---
title: "CRecordset::CanRestart"
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
ms.assetid: 1ba85ff9-28bb-4ac5-a226-63119dc8f55d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::CanRestart
Determines whether the recordset allows restarting its query (to refresh its records) by calling the **Requery** member function.  
  
## Syntax  
  
```  
  
BOOL CanRestart( ) const;  
```  
  
## Return Value  
 Nonzero if requery is allowed; otherwise 0.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::Requery](../vs140/CRecordset--Requery.md)