---
title: "CDC::FillRgn"
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
ms.assetid: f40489dc-526a-4917-b265-25120bfb1167
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::FillRgn
Fills the region specified by `pRgn` with the brush specified by `pBrush`.  
  
## Syntax  
  
```  
  
      BOOL FillRgn(  
   CRgn* pRgn,  
   CBrush* pBrush   
);  
```  
  
#### Parameters  
 `pRgn`  
 A pointer to the region to be filled. The coordinates for the given region are specified in logical units.  
  
 `pBrush`  
 Identifies the brush to be used to fill the region.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The brush must either be created using the `CBrush` member functions `CreateHatchBrush`, `CreatePatternBrush`, `CreateSolidBrush`, or be retrieved by **GetStockObject**.  
  
## Example  
 See the example for [CRgn::CreateRoundRectRgn](../vs140/CRgn--CreateRoundRectRgn.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::PaintRgn](../vs140/CDC--PaintRgn.md)   
 [CDC::FillRect](../vs140/CDC--FillRect.md)   
 [CBrush Class](../vs140/CBrush-Class.md)   
 [CRgn Class](../vs140/CRgn-Class.md)   
 [FillRgn](http://msdn.microsoft.com/library/windows/desktop/dd162720)