---
title: "CDaoQueryDef::GetRecordsAffected"
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
ms.assetid: bf338492-0231-44e2-9611-e026cf88501e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetRecordsAffected
Call this member function to determine how many records were affected by the last call of [Execute](../vs140/CDaoQueryDef--Execute.md).  
  
## Syntax  
  
```  
  
long GetRecordsAffected( );  
  
```  
  
## Return Value  
 The number of records affected.  
  
## Remarks  
 The count returned will not reflect changes in related tables when cascade updates or deletes are in effect.  
  
 For related information see the topic "RecordsAffected Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)