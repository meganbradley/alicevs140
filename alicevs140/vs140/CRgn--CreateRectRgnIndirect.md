---
title: "CRgn::CreateRectRgnIndirect"
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
ms.assetid: bee552f6-4d74-40f0-8f23-fcd8c823b988
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::CreateRectRgnIndirect
Creates a rectangular region that is stored in the `CRgn` object.  
  
## Syntax  
  
```  
  
      BOOL CreateRectRgnIndirect(  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `lpRect`  
 Points to a `RECT` structure or `CRect` object that contains the logical coordinates of the upper-left and lower-right corners of the region. The `RECT` structure has the following form:  
  
 `typedef struct tagRECT {`  
  
 `int left;`  
  
 `int top;`  
  
 `int right;`  
  
 `int bottom;`  
  
 `} RECT;`  
  
## Return Value  
 Nonzero if the operation succeeded; otherwise 0.  
  
## Remarks  
 The size of a region is limited to 32,767 by 32,767 logical units or 64K of memory, whichever is smaller.  
  
 When it has finished using a region created by `CreateRectRgnIndirect`, an application should use the [CGDIObject::DeleteObject](../vs140/CGdiObject--DeleteObject.md) member function to remove the region.  
  
## Example  
 [!CODE [NVC_MFCDocView#148](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#148)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRgn::CreateRectRgn](../vs140/CRgn--CreateRectRgn.md)   
 [CRgn::CreateRoundRectRgn](../vs140/CRgn--CreateRoundRectRgn.md)   
 [CreateRectRgnIndirect](http://msdn.microsoft.com/library/windows/desktop/dd183515)