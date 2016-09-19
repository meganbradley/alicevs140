---
title: "CAnimationVariable::EnableIntegerValueChangedEvent"
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
ms.assetid: 20c6d481-fd8c-4216-bffa-ec18334934a3
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationVariable::EnableIntegerValueChangedEvent
Enables or disables the IntegerValueChanged event.  
  
## Syntax  
  
```  
void EnableIntegerValueChangedEvent (  
   CAnimationController* pController,  
   BOOL bEnable  
);  
```  
  
#### Parameters  
 `pController`  
 A pointer to parent controller.  
  
 `bEnable`  
 TRUE - enable event, FALSE - disable event.  
  
## Remarks  
 When ValueChanged event is enabled, the framework calls virtual method CAnimationController::OnAnimationIntegerValueChanged. You need to override it in a class derived from CAnimationController in order to process this event. This method is called every time the integer value of animation variable is changed.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationVariable Class](../vs140/CAnimationVariable-Class.md)