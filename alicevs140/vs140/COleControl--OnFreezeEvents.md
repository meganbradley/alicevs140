---
title: "COleControl::OnFreezeEvents"
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
ms.assetid: 459a3116-a55e-4707-b691-3575126fbb8d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnFreezeEvents
Called by the framework after the container calls **IOleControl::FreezeEvents**.  
  
## Syntax  
  
```  
  
      virtual void OnFreezeEvents(  
   BOOL bFreeze   
);  
```  
  
#### Parameters  
 `bFreeze`  
 **TRUE** if the control's event handling is frozen; otherwise **FALSE**.  
  
## Remarks  
 The default implementation does nothing.  
  
 Override this function if you want additional behavior when event handling is frozen or unfrozen.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)