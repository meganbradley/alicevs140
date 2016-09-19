---
title: "CDockablePane::GetDragSensitivity"
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
ms.assetid: 442252df-773f-4e9e-b580-436381ebcfd1
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::GetDragSensitivity
Returns the drag sensitivity of a docking pane.  
  
## Syntax  
  
```  
static const CSize& GetDragSensitivity();  
```  
  
## Return Value  
 A [CSize](../vs140/CSize-Class.md) object that contains the width and height, in pixels, of a rectangle centered on a drag point. The drag operation does not begin until the mouse pointer moves outside this rectangle.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)