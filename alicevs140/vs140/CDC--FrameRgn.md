---
title: "CDC::FrameRgn"
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
ms.assetid: 994d2c49-67f3-4674-b72c-1907b920b567
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::FrameRgn
Draws a border around the region specified by `pRgn` using the brush specified by `pBrush`.  
  
## Syntax  
  
```  
  
      BOOL FrameRgn(  
   CRgn* pRgn,  
   CBrush* pBrush,  
   int nWidth,  
   int nHeight   
);  
```  
  
#### Parameters  
 `pRgn`  
 Points to the `CRgn` object that identifies the region to be enclosed in a border. The coordinates for the given region are specified in logical units.  
  
 `pBrush`  
 Points to the `CBrush` object that identifies the brush to be used to draw the border.  
  
 `nWidth`  
 Specifies the width of the border in vertical brush strokes in device units.  
  
 `nHeight`  
 Specifies the height of the border in horizontal brush strokes in device units.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Example  
 See the example for [CRgn::CombineRgn](../vs140/CRgn--CombineRgn.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Rectangle](../vs140/CDC--Rectangle.md)   
 [CDC::FrameRect](../vs140/CDC--FrameRect.md)   
 [CBrush Class](../vs140/CBrush-Class.md)   
 [CRgn Class](../vs140/CRgn-Class.md)   
 [FrameRgn](http://msdn.microsoft.com/library/windows/desktop/dd144839)