---
title: "CAnimationController::OnAnimationTimerPreUpdate"
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
ms.assetid: 72508236-9625-4a3e-83cf-34c9f9fb4143
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::OnAnimationTimerPreUpdate
Called by the framework before an animation update begins.  
  
## Syntax  
  
```  
virtual void OnAnimationTimerPreUpdate();  
```  
  
## Remarks  
 This method is called if you enable timer event handlers using EnableAnimationTimerEventHandler. It can be overridden in a derived class to take application-specific actions.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)