---
title: "CRgn::CreateRectRgn"
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
ms.assetid: 97d03fc8-cbcc-47a0-a336-ccf5f988ff7e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::CreateRectRgn
Creates a rectangular region that is stored in the `CRgn` object.  
  
## Syntax  
  
```  
  
      BOOL CreateRectRgn(  
   int x1,  
   int y1,  
   int x2,  
   int y2   
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
  
## Return Value  
 Nonzero if the operation succeeded; otherwise 0.  
  
## Remarks  
 The size of a region is limited to 32,767 by 32,767 logical units or 64K of memory, whichever is smaller.  
  
 When it has finished using a region created by `CreateRectRgn`, an application should use the [CGDIObject::DeleteObject](../vs140/CGdiObject--DeleteObject.md) member function to remove the region.  
  
## Example  
 [!CODE [NVC_MFCDocView#147](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#147)]  
  
 For an additional example, see [CRgn::CombineRgn](../vs140/CRgn--CombineRgn.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRgn::CreateRectRgnIndirect](../vs140/CRgn--CreateRectRgnIndirect.md)   
 [CRgn::CreateRoundRectRgn](../vs140/CRgn--CreateRoundRectRgn.md)   
 [CreateRectRgn](http://msdn.microsoft.com/library/windows/desktop/dd183514)