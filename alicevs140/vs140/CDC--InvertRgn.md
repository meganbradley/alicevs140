---
title: "CDC::InvertRgn"
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
ms.assetid: cfb6c105-a1b7-4f2b-ba30-250d0b3761bc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::InvertRgn
Inverts the colors in the region specified by `pRgn`.  
  
## Syntax  
  
```  
  
      BOOL InvertRgn(  
   CRgn* pRgn   
);  
```  
  
#### Parameters  
 `pRgn`  
 Identifies the region to be inverted. The coordinates for the region are specified in logical units.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 On monochrome displays, the function makes white pixels black and black pixels white. On color displays, the inversion depends on how the colors are generated for the display.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::FillRgn](../vs140/CDC--FillRgn.md)   
 [CDC::PaintRgn](../vs140/CDC--PaintRgn.md)   
 [CRgn Class](../vs140/CRgn-Class.md)   
 [InvertRgn](http://msdn.microsoft.com/library/windows/desktop/dd145008)