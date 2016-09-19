---
title: "CDaoQueryDef::GetFieldCount"
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
ms.assetid: 1184b443-630a-438e-b2a4-d8efccb2a992
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetFieldCount
Call this member function to retrieve the number of fields in the query.  
  
## Syntax  
  
```  
  
short GetFieldCount( );  
  
```  
  
## Return Value  
 The number of fields defined in the query.  
  
## Remarks  
 `GetFieldCount` is useful for looping through all fields in the querydef. For that purpose, use `GetFieldCount` in conjunction with [GetFieldInfo](../vs140/CDaoQueryDef--GetFieldInfo.md).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)