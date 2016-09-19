---
title: "CAnimationGroup::FindAnimationObject"
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
ms.assetid: e2b6f53f-c1a2-4c50-843b-c9665c2d1949
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationGroup::FindAnimationObject
Finds an animation object that contains the specified animation variable.  
  
## Syntax  
  
```  
CAnimationBaseObject* FindAnimationObject(  
   IUIAnimationVariable* pVariable  
);  
```  
  
#### Parameters  
 `pVariable`  
 A pointer to animation variable.  
  
## Return Value  
 A pointer to animation object, or NULL if animation object is not found.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationGroup Class](../vs140/CAnimationGroup-Class.md)