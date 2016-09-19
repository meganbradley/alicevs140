---
title: "CAnimationController::EnableStoryboardEventHandler"
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
ms.assetid: 6f3f5c6a-7895-4979-a0f3-7e669a290d87
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::EnableStoryboardEventHandler
Sets or releases a handler for storyboard status and update events.  
  
## Syntax  
  
```  
virtual BOOL EnableStoryboardEventHandler(  
   UINT32 nGroupID,  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 `nGroupID`  
 Specifies Group ID.  
  
 `bEnable`  
 Specifies whether to set or release a handler.  
  
## Return Value  
 TRUE if the handler was successfully set or released; FALSE if the specified animation group is now found or animation for the specified group has not been initiated and its internal storyboard is NULL.  
  
## Remarks  
 When a handler is set (enabled) Windows Animation API calls OnStoryboardStatusChanges and OnStoryboardUpdated virtual methods. A handler must be set after CAnimationController::Animate has been called for the specified animation group, because it creates encapsulated IUIAnimationStoryboard object.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)