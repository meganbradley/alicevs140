---
title: "CControlBar::DoPaint"
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
ms.assetid: 0be69066-9031-4040-b834-76544d966354
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::DoPaint
Called by the framework to render the borders and gripper bar of the control bar.  
  
## Syntax  
  
```  
  
      virtual void DoPaint(  
   CDC* pDC   
);  
```  
  
#### Parameters  
 `pDC`  
 Points to the device context to be used for rendering the borders and gripper of the control bar.  
  
## Remarks  
 Override this function to customize the drawing behavior of the control bar.  
  
 Another customization method is to override the `DrawBorders` and `DrawGripper` functions and add custom drawing code for the borders and gripper. Because these methods are called by the default `DoPaint` method, an override of `DoPaint` is not needed.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CControlBar::DrawBorders](../vs140/CControlBar--DrawBorders.md)   
 [CControlBar::DrawGripper](../vs140/CControlBar--DrawGripper.md)