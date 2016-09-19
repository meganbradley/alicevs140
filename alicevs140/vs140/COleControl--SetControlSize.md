---
title: "COleControl::SetControlSize"
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
ms.assetid: 87b0b3bc-12dd-4c10-98fa-32c67c7bcfa7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetControlSize
Sets the size of the OLE control window and notifies the container that the control site is changing.  
  
## Syntax  
  
```  
  
      BOOL SetControlSize(  
   int cx,  
   int cy   
);  
```  
  
#### Parameters  
 `cx`  
 Specifies the new width of the control in pixels.  
  
 `cy`  
 Specifies the new height of the control in pixels.  
  
## Return Value  
 Nonzero if the call was successful; otherwise 0.  
  
## Remarks  
 This function should not be used in your control's constructor.  
  
 Note that all coordinates for control windows are relative to the upper-left corner of the control.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetControlSize](../vs140/COleControl--GetControlSize.md)   
 [COleControl::GetRectInContainer](../vs140/COleControl--GetRectInContainer.md)