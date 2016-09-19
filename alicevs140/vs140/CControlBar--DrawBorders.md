---
title: "CControlBar::DrawBorders"
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
ms.assetid: 9bc74946-2d92-4a6b-88fb-a9d0739fa840
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::DrawBorders
Called by the framework to render the borders of the control bar.  
  
## Syntax  
  
```  
  
      virtual void DrawBorders(  
   CDC* pDC,  
   CRect& rect   
);  
```  
  
#### Parameters  
 `pDC`  
 Points to the device context to be used for rendering the borders of the control bar.  
  
 `rect`  
 A `CRect` object containing the dimensions of the control bar.  
  
## Remarks  
 Override this function to customize the appearance of the control bar borders.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CControlBar::DoPaint](../vs140/CControlBar--DoPaint.md)   
 [CControlBar::DrawGripper](../vs140/CControlBar--DrawGripper.md)