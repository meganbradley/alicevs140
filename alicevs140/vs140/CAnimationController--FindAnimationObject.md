---
title: "CAnimationController::FindAnimationObject"
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
ms.assetid: f65fd825-7b2b-4b40-980e-ea343515e908
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::FindAnimationObject
Finds animation object containing a specified animation variable.  
  
## Syntax  
  
```  
BOOL FindAnimationObject(  
   IUIAnimationVariable* pVariable,  
   CAnimationBaseObject** ppObject,  
   CAnimationGroup** ppGroup  
);  
```  
  
#### Parameters  
 `pVariable`  
 A pointer to animation variable.  
  
 `ppObject`  
 Output. Contains a pointer to animation object or NULL.  
  
 `ppGroup`  
 Output. Contains a pointer to animation group that holds the animation object, or NULL.  
  
## Return Value  
 TRUE if object was found; otherwise FALSE.  
  
## Remarks  
 Called from event handlers when it's required to find an animation object from incoming animation variable.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)