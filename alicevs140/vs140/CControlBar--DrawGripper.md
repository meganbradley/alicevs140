---
title: "CControlBar::DrawGripper"
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
ms.assetid: fc662551-8dfb-412d-ba02-115801c03a98
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::DrawGripper
Called by the framework to render the gripper of the control bar.  
  
## Syntax  
  
```  
  
      virtual void DrawGripper(  
   CDC* pDC,  
   const CRect& rect   
);  
```  
  
#### Parameters  
 `pDC`  
 Points to the device context to be used for rendering the control bar gripper.  
  
 `rect`  
 A `CRect` object containing the dimensions of the control bar gripper.  
  
## Remarks  
 Override this function to customize the appearance of the control bar gripper.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CControlBar::DoPaint](../vs140/CControlBar--DoPaint.md)   
 [CControlBar::DrawBorders](../vs140/CControlBar--DrawBorders.md)