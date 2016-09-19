---
title: "CDrawingManager::DrawEllipse"
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
ms.assetid: 655c9ca6-4d4d-4269-9616-3a97cfbe0f6e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::DrawEllipse
Draws an ellipse with the supplied fill and border colors.  
  
## Syntax  
  
```  
void DrawEllipse(  
   const CRect& rect,  
   COLORREF clrFill,  
   COLORREF clrLine  
);  
```  
  
#### Parameters  
 [in] `rect`  
 The bounding rectangle for the ellipse.  
  
 [in] `clrFill`  
 The color this method uses to fill the ellipse.  
  
 [in] `clrLine`  
 The color this method uses as the border of the ellipse.  
  
## Remarks  
 This method returns without drawing an ellipse if either color is set to -1. It also returns without drawing an ellipse if either dimension of the bounding rectangle is 0.  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)