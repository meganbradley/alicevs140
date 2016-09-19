---
title: "CAnimationBaseObject::EnableIntegerValueChangedEvent"
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
ms.assetid: e33921bb-090c-46dc-b102-63d72a894b10
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::EnableIntegerValueChangedEvent
Sets up Integer Value Changed event handler.  
  
## Syntax  
  
```  
virtual void EnableIntegerValueChangedEvent(  
   CAnimationController* pController,  
   BOOL bEnable  
);  
```  
  
#### Parameters  
 `pController`  
 A pointer to a parent controller.  
  
 `bEnable`  
 Specifies whether to enable, or disable Integer Value Changed event.  
  
## Remarks  
 If the Integer Value Changed event handler is enabled, you can handle this event in CAnimationController::OnAnimationIntegerValueChanged method, which should be overridden in a CAnimationController-derived class. This method is called every time the animation integer value has changed.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)