---
title: "CRgn::CreateEllipticRgnIndirect"
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
ms.assetid: 2f44d9d2-6acc-44ce-b236-b60f540b8e28
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::CreateEllipticRgnIndirect
Creates an elliptical region.  
  
## Syntax  
  
```  
  
      BOOL CreateEllipticRgnIndirect(  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `lpRect`  
 Points to a `RECT` structure or a `CRect` object that contains the logical coordinates of the upper-left and lower-right corners of the bounding rectangle of the ellipse.  
  
## Return Value  
 Nonzero if the operation succeeded; otherwise 0.  
  
## Remarks  
 The region is defined by the structure or object pointed to by `lpRect` and is stored in the `CRgn` object.  
  
 The size of a region is limited to 32,767 by 32,767 logical units or 64K of memory, whichever is smaller.  
  
 When it has finished using a region created with the `CreateEllipticRgnIndirect` function, an application should select the region out of the device context and use the `DeleteObject` function to remove it.  
  
## Example  
 See the example for [CRgn::CreateRectRgnIndirect](../vs140/CRgn--CreateRectRgnIndirect.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRgn::CreateEllipticRgn](../vs140/CRgn--CreateEllipticRgn.md)   
 [CreateEllipticRgnIndirect](http://msdn.microsoft.com/library/windows/desktop/dd183497)