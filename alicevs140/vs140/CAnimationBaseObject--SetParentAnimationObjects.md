---
title: "CAnimationBaseObject::SetParentAnimationObjects"
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
ms.assetid: 886b6b9e-ca02-48f3-ba5c-3c8e748fe5d8
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::SetParentAnimationObjects
Establishes relationship between animation variables, contained in an animation object, and their container.  
  
## Syntax  
  
```  
virtual void SetParentAnimationObjects();  
```  
  
## Remarks  
 This is a helper that can be used to establish relationship between animation variables, contained in an animation object, and their container. It loops over animation variables and sets a back pointer to a parent animation object to each animation variable. In the current implementation the actual relationship is established in CAnimationBaseObject::ApplyTransitions, therefore back pointers are not set until you call CAnimationGroup::Animate. Knowing the relationship may be helpful when you processing events and need to get a parent animation object from CAnimationVariable (use CAnimationVariable::GetParentAnimationObject).  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)