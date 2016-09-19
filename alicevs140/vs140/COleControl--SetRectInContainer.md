---
title: "COleControl::SetRectInContainer"
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
ms.assetid: 443f3114-b5c8-4279-9baf-cb3735bd8ee2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetRectInContainer
Sets the coordinates of the control's rectangle relative to the container, expressed in device units.  
  
## Syntax  
  
```  
  
      BOOL SetRectInContainer(  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `lpRect`  
 A pointer to a rectangle containing the control's new coordinates relative to the container.  
  
## Return Value  
 Nonzero if the call was successful; otherwise 0.  
  
## Remarks  
 If the control is open, it is resized; otherwise the container's **OnPosRectChanged** function is called.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetRectInContainer](../vs140/COleControl--GetRectInContainer.md)   
 [COleControl::GetControlSize](../vs140/COleControl--GetControlSize.md)