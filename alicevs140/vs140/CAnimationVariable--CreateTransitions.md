---
title: "CAnimationVariable::CreateTransitions"
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
ms.assetid: 70b99aa2-955a-40cf-be3b-c5ba8b918eff
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationVariable::CreateTransitions
Creates all transitions to be applied to this animation variable.  
  
## Syntax  
  
```  
BOOL CreateTransitions(  
   IUIAnimationTransitionLibrary* pLibrary,  
   IUIAnimationTransitionFactory* pFactory  
);  
```  
  
#### Parameters  
 `pLibrary`  
 A pointer to transition library.  
  
 `pFactory`  
 A pointer to transition factory.  
  
## Return Value  
 TRUE if transitions were created successfully; otherwise FALSE.  
  
## Remarks  
 This method is called by the framework when it needs to create transitions that have been added to the variable's internal list of transitions.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationVariable Class](../vs140/CAnimationVariable-Class.md)