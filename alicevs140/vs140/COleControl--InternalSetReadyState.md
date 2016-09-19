---
title: "COleControl::InternalSetReadyState"
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
ms.assetid: 7d8f85a9-ee2c-4f51-8418-3a2ae61fa26c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::InternalSetReadyState
Sets the readiness state of the control.  
  
## Syntax  
  
```  
  
      void InternalSetReadyState(  
   long lNewReadyState   
);  
```  
  
#### Parameters  
 *lNewReadyState*  
 The readiness state to set for the control, one of the following values:  
  
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
 [COleControl::GetReadyState](../vs140/COleControl--GetReadyState.md)