---
title: "CMultiLock::IsLocked"
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
ms.assetid: 7bf6520f-92d2-473c-9ef4-075a0e77b5b9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMultiLock::IsLocked
Determines if the specified object is nonsignaled (unavailable).  
  
## Syntax  
  
```  
  
      BOOL IsLocked(  
   DWORD dwItem   
);  
```  
  
#### Parameters  
 *dwItem*  
 The index in the array of objects corresponding to the object whose state is being queried.  
  
## Return Value  
 Nonzero if the specified object is locked; otherwise 0.  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CMultiLock Class](../vs140/CMultiLock-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)