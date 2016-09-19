---
title: "CRgn::CreateRoundRectRgn"
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
ms.assetid: 691599de-0705-49a3-9bcd-eca86051b290
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::CreateRoundRectRgn
Creates a rectangular region with rounded corners that is stored in the `CRgn` object.  
  
## Syntax  
  
```  
  
      BOOL CreateRoundRectRgn(  
   int x1,  
   int y1,  
   int x2,  
   int y2,  
   int x3,  
   int y3   
);  
```  
  
#### Parameters  
 `x1`  
 Specifies the logical x-coordinate of the upper-left corner of the region.  
  
 `y1`  
 Specifies the logical y-coordinate of the upper-left corner of the region.  
  
 `x2`  
 Specifies the logical x-coordinate of the lower-right corner of the region.  
  
 `y2`  
 Specifies the logical y-coordinate of the lower-right corner of the region.  
  
 *x3*  
 Specifies the width of the ellipse used to create the rounded corners.  
  
 `y3`  
 Specifies the height of the ellipse used to create the rounded corners.  
  
## Return Value  
 Nonzero if the operation succeeded; otherwise 0.  
  
## Remarks  
 The size of a region is limited to 32,767 by 32,767 logical units or 64K of memory, whichever is smaller.  
  
 When an application has finished using a region created with the `CreateRoundRectRgn` function, it should select the region out of the device context and use the [CGDIObject::DeleteObject](../vs140/CGdiObject--DeleteObject.md) member function to remove it.  
  
## Example  
 [!CODE [NVC_MFCDocView#149](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#149)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRgn::CreateRectRgn](../vs140/CRgn--CreateRectRgn.md)   
 [CRgn::CreateRectRgnIndirect](../vs140/CRgn--CreateRectRgnIndirect.md)   
 [CreateRoundRectRgn](http://msdn.microsoft.com/library/windows/desktop/dd183516)