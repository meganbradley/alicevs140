---
title: "CAnimationTimerEventHandler::SetAnimationController"
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
ms.assetid: 5847e1c7-8d73-4773-92e0-ac8e108ff1d2
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationTimerEventHandler::SetAnimationController
Stores a pointer to animation controller to route events.  
  
## Syntax  
  
```  
void SetAnimationController(  
   CAnimationController* pAnimationController  
);  
```  
  
#### Parameters  
 `pAnimationController`  
 A pointer to animation controller, which will receive events.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationTimerEventHandler Class](../vs140/CAnimationTimerEventHandler-Class.md)