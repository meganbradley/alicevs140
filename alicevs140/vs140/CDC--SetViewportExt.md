---
title: "CDC::SetViewportExt"
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
ms.assetid: eba2b828-7620-4c9d-80e6-707d21d8f6ad
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetViewportExt
Sets the x- and y-extents of the viewport of the device context.  
  
## Syntax  
  
```  
  
      virtual CSize SetViewportExt(  
   int cx,  
   int cy   
);  
CSize SetViewportExt(  
   SIZE size   
);  
```  
  
#### Parameters  
 `cx`  
 Specifies the x-extent of the viewport (in device units).  
  
 `cy`  
 Specifies the y-extent of the viewport (in device units).  
  
 `size`  
 Specifies the x- and y-extents of the viewport (in device units).  
  
## Return Value  
 The previous extents of the viewport as a [CSize](../vs140/CSize-Class.md) object. When an error occurs, the x- and y-coordinates of the returned `CSize` object are both set to 0.  
  
## Remarks  
 The viewport, along with the device-context window, defines how GDI maps points in the logical coordinate system to points in the coordinate system of the actual device. In other words, they define how GDI converts logical coordinates into device coordinates.  
  
 When the following mapping modes are set, calls to `SetWindowExt` and `SetViewportExt` are ignored:  
  
|MM_HIENGLISH|MM_LOMETRIC|  
|-------------------|------------------|  
|`MM_HIMETRIC`|`MM_TEXT`|  
|`MM_LOENGLISH`|`MM_TWIPS`|  
  
 When `MM_ISOTROPIC` mode is set, an application must call the `SetWindowExt` member function before it calls `SetViewportExt`.  
  
## Example  
 See the example for [CView::OnPrepareDC](../vs140/CView--OnPrepareDC.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetWindowExt](../vs140/CDC--SetWindowExt.md)   
 [CSize Class](../vs140/CSize-Class.md)   
 [CDC::GetViewportExt](../vs140/CDC--GetViewportExt.md)