---
title: "COleControl::OnEventAdvise"
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
ms.assetid: ebb1331e-919b-4b2c-9e46-0f32e2d5fa9a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnEventAdvise
Called by the framework when an event handler is connected to or disconnected from an OLE control.  
  
## Syntax  
  
```  
  
      virtual void OnEventAdvise(  
   BOOL bAdvise   
);  
```  
  
#### Parameters  
 `bAdvise`  
 **TRUE** indicates that an event handler has been connected to the control. **FALSE** indicates that an event handler has been disconnected from the control.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)