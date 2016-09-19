---
title: "CDC::PaintRgn"
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
ms.assetid: f7870834-a3d2-47ab-99bd-ef0b3ef56e32
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::PaintRgn
Fills the region specified by `pRgn` using the current brush.  
  
## Syntax  
  
```  
  
      BOOL PaintRgn(  
   CRgn* pRgn   
);  
```  
  
#### Parameters  
 `pRgn`  
 Identifies the region to be filled. The coordinates for the given region are specified in logical units.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBrush Class](../vs140/CBrush-Class.md)   
 [CDC::SelectObject](../vs140/CDC--SelectObject.md)   
 [CDC::FillRgn](../vs140/CDC--FillRgn.md)   
 [PaintRgn](http://msdn.microsoft.com/library/windows/desktop/dd162767)   
 [CRgn Class](../vs140/CRgn-Class.md)