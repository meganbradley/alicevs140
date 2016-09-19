---
title: "CDatabase::CanUpdate"
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
ms.assetid: 0366d19d-b36f-46f7-8eac-eb359c6c2fc4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::CanUpdate
Call this member function to determine whether the `CDatabase` object allows updates.  
  
## Syntax  
  
```  
  
BOOL CanUpdate( ) const;  
```  
  
## Return Value  
 Nonzero if the `CDatabase` object allows updates; otherwise 0, indicating either that you passed **TRUE** in `bReadOnly` when you opened the `CDatabase` object or that the data source itself is read-only. The data source is read-only if a call to the ODBC API function **SQLGetInfo** for **SQL_DATASOURCE_READ_ONLY** returns "y".  
  
## Remarks  
 Not all drivers support updates.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)