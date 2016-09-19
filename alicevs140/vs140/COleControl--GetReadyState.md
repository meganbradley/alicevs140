---
title: "COleControl::GetReadyState"
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
ms.assetid: 601fd1bf-cfd9-45ac-bf5c-281b67134432
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetReadyState
Returns the readiness state of the control.  
  
## Syntax  
  
```  
  
long GetReadyState( );  
```  
  
## Return Value  
 The readiness state of the control, one of the following values:  
  
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
  
## Remarks  
 Most simple controls never need to differentiate between **LOADED** and `INTERACTIVE`. However, controls that support data path properties may not be ready to be interactive until at least some data is received asynchronously. A control should attempt to become interactive as soon as possible.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::FireReadyStateChange](../vs140/COleControl--FireReadyStateChange.md)   
 [COleControl::InternalSetReadyState](../vs140/COleControl--InternalSetReadyState.md)