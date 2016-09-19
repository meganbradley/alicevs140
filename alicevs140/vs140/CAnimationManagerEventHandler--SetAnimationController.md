---
title: "CAnimationManagerEventHandler::SetAnimationController"
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
ms.assetid: d3176ce4-1e2c-464b-b4ab-410793057527
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationManagerEventHandler::SetAnimationController
[!INCLUDE[dev10_sp1required](../vs140/includes/dev10_sp1required_md.md)]  
  
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
 [CAnimationManagerEventHandler Class](../vs140/CAnimationManagerEventHandler-Class.md)