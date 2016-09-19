---
title: "CDaoQueryDef::IsOpen"
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
ms.assetid: 8d60c0d2-0181-480f-b213-439e2324f3cf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::IsOpen
Call this member function to determine whether the `CDaoQueryDef` object is currently open.  
  
## Syntax  
  
```  
  
BOOL IsOpen( ) const;  
  
```  
  
## Return Value  
 Nonzero if the `CDaoQueryDef` object is currently open; otherwise 0.  
  
## Remarks  
 A querydef must be in an open state before you use it to call [Execute](../vs140/CDaoQueryDef--Execute.md) or to create a [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object. To put a querydef into an open state call either [Create](../vs140/CDaoQueryDef--Create.md) (for a new querydef) or [Open](../vs140/CDaoQueryDef--Open.md) (for an existing querydef).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)