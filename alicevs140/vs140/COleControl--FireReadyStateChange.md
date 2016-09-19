---
title: "COleControl::FireReadyStateChange"
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
ms.assetid: c003aa5f-f871-48dd-a3d8-dfc0dae91047
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::FireReadyStateChange
Fires an event with the current value of the ready state of control.  
  
## Syntax  
  
```  
  
void FireReadyStateChange( );  
```  
  
## Remarks  
 The ready state can be one of the following values:  
  
 **READYSTATE_UNINITIALIZED**  
 Default initialization state  
  
 **READYSTATE_LOADING**  
 Control is currently loading its properties  
  
 **READYSTATE_LOADED**  
 Control has been initialized  
  
 **READYSTATE_INTERACTIVE**  
 Control has enough data to be interactive but not all asynchronous data is yet loaded  
  
 `READYSTATE_COMPLETE`  
 Control has all its data  
  
 Use [GetReadyState](../vs140/COleControl--GetReadyState.md) to determine the control's current readiness.  
  
 [InternalSetReadyState](../vs140/COleControl--InternalSetReadyState.md) changes the ready state to the value supplied, then calls `FireReadyStateChange`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetReadyState](../vs140/COleControl--GetReadyState.md)   
 [COleControl::InternalSetReadyState](../vs140/COleControl--InternalSetReadyState.md)