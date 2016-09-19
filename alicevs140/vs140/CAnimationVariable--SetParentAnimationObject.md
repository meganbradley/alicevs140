---
title: "CAnimationVariable::SetParentAnimationObject"
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
ms.assetid: e338850d-b8f1-4b69-934b-75dc3baf525a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationVariable::SetParentAnimationObject
Sets the relationship between an animation variable and an animation object.  
  
## Syntax  
  
```  
void SetParentAnimationObject(  
   CAnimationBaseObject* pParentObject  
);  
```  
  
#### Parameters  
 `pParentObject`  
 A pointer to an animation object that contains this variable.  
  
## Remarks  
 This method is called internally to establish one-to-one relationship between an animation variable and an animation object that encapsulates it.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationVariable Class](../vs140/CAnimationVariable-Class.md)