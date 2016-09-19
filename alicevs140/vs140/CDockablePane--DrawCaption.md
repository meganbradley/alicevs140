---
title: "CDockablePane::DrawCaption"
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
ms.assetid: 1ec46d53-dcb6-4aea-9d6f-69c762b0367b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::DrawCaption
Draws the caption (also called the gripper) of a docking pane.  
  
## Syntax  
  
```  
virtual void DrawCaption(  
    CDC* pDC,  
    CRect rectCaption  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Represents the device context used for drawing.  
  
 [in] `rectCaption`  
 Specifies the bounding rectangle of the pane's caption.  
  
## Remarks  
 The framework calls this method to draw the caption of a dockable pane.  
  
 Override this method in a derived class to customize the appearance of the caption.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)