---
title: "CAnimationController::RemoveTransitions"
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
ms.assetid: ac3c2c87-033b-4747-a4e6-1a10ee097227
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::RemoveTransitions
Removes transitions from animation objects that belong to the specified group.  
  
## Syntax  
  
```  
void RemoveTransitions(  
   UINT32 nGroupID  
);  
```  
  
#### Parameters  
 `nGroupID`  
 Specifies Group ID.  
  
## Remarks  
 The group loops over its animation objects and calls ClearTransitions(FALSE) for each animation object. This method is called by the framework after animation has been scheduled.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)