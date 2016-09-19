---
title: "CDC::Draw3dRect"
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
ms.assetid: d733b008-cccd-40b7-b4ee-40355e94dc64
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::Draw3dRect
Call this member function to draw a three-dimensional rectangle.  
  
## Syntax  
  
```  
  
      void Draw3dRect(  
   LPCRECT lpRect,  
   COLORREF clrTopLeft,  
   COLORREF clrBottomRight   
);  
void Draw3dRect(  
   int x,  
   int y,  
   int cx,  
   int cy,  
   COLORREF clrTopLeft,  
   COLORREF clrBottomRight   
);  
```  
  
#### Parameters  
 `lpRect`  
 Specifies the bounding rectangle (in logical units). You can pass either a pointer to a [RECT](../vs140/RECT-Structure.md) structure or a [CRect](../vs140/CRect-Class.md) object for this parameter.  
  
 *clrTopLeft*  
 Specifies the color of the top and left sides of the three-dimensional rectangle.  
  
 `clrBottomRight`  
 Specifies the color of the bottom and right sides of the three-dimensional rectangle.  
  
 *x*  
 Specifies the logical x-coordinate of the upper-left corner of the three-dimensional rectangle.  
  
 *y*  
 Specifies the logical y-coordinate of the upper-left corner of the three-dimensional rectangle.  
  
 cx  
 Specifies the width of the three-dimensional rectangle.  
  
 cy  
 Specifies the height of the three-dimensional rectangle.  
  
## Remarks  
 The rectangle will be drawn with the top and left sides in the color specified by *clrTopLeft* and the bottom and right sides in the color specified by `clrBottomRight`.  
  
## Example  
 [!CODE [NVC_MFCDocView#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#33)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [RECT Structure](../vs140/RECT-Structure.md)   
 [CRect Class](../vs140/CRect-Class.md)