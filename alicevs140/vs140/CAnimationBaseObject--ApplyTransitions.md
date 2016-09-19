---
title: "CAnimationBaseObject::ApplyTransitions"
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
ms.assetid: 5a85f3ed-61fa-4a7e-b74a-ba91dca607b8
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::ApplyTransitions
Adds transitions to storyboard with encapsulated animation variable.  
  
## Syntax  
  
```  
virtual BOOL ApplyTransitions(  
   IUIAnimationStoryboard* pStoryboard,  
   BOOL bDependOnKeyframes  
);  
```  
  
#### Parameters  
 `pStoryboard`  
 A pointer to a storyboard.  
  
 `bDependOnKeyframes`  
 With FALSE this method adds only those transitions that do not depend on keyframes.  
  
## Return Value  
 TRUE if transitions were added successfully.  
  
## Remarks  
 Adds related transitions, that have been added with AddTransition (overloaded methods in derived classes), to storyboard.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)