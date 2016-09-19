---
title: "CAnimationController::RemoveAnimationObject"
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
ms.assetid: 770ec11f-9bce-4fb0-b966-1d6530d779eb
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::RemoveAnimationObject
Remove an animation object from animation controller.  
  
## Syntax  
  
```  
void RemoveAnimationObject(  
   CAnimationBaseObject* pObject,  
   BOOL bNoDelete = FALSE  
);  
```  
  
#### Parameters  
 `pObject`  
 A pointer to an animation object.  
  
 `bNoDelete`  
 If this parameter is TRUE the object will not be deleted upon remove.  
  
## Remarks  
 Removes an animation object from animation controller and animation group. Call this function if a particular object should not be animated anymore, or if you need to move the object to another animation controller. In the last case bNoDelete must be TRUE.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)