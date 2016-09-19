---
title: "CDaoTableDef::CanUpdate"
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
ms.assetid: 4937f537-2973-4503-a7b9-e57b4fbeebc9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::CanUpdate
Call this member function to determine whether the definition of the table underlying a `CDaoTableDef` object can be changed.  
  
## Syntax  
  
```  
  
BOOL CanUpdate( );  
  
```  
  
## Return Value  
 Nonzero if the table structure (schema) can be modified (add or delete fields and indexes), otherwise 0.  
  
## Remarks  
 By default, a newly created table underlying a `CDaoTableDef` object can be updated, and an attached table underlying a `CDaoTableDef` object cannot be updated. A `CDaoTableDef` object may be updatable, even if the resulting recordset is not updatable.  
  
 For related information, see the topic "Updatable Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::GetDateLastUpdated](../vs140/CDaoTableDef--GetDateLastUpdated.md)