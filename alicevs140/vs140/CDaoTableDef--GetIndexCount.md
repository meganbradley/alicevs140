---
title: "CDaoTableDef::GetIndexCount"
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
ms.assetid: db12476a-5f00-4eda-94e5-ddfd75d0341a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::GetIndexCount
Call this member function to obtain the number of indexes for a table.  
  
## Syntax  
  
```  
  
short GetIndexCount( );  
  
```  
  
## Return Value  
 The number of indexes for the table.  
  
## Remarks  
 If its value is 0, there are no indexes in the collection.  
  
 For related information, see the topic "Count Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::GetIndexInfo](../vs140/CDaoTableDef--GetIndexInfo.md)   
 [CDaoTableDef::GetFieldInfo](../vs140/CDaoTableDef--GetFieldInfo.md)   
 [CDaoTableDef::GetFieldCount](../vs140/CDaoTableDef--GetFieldCount.md)