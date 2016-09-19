---
title: "ATL_DRAWINFO Structure"
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
ms.topic: article
ms.assetid: dd2e2aa8-e8c5-403b-b4df-35c0f6f57fb7
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL_DRAWINFO Structure
Contains information used for rendering to various targets, such as a printer, metafile, or ActiveX control.  
  
## Syntax  
  
```  
  
      struct ATL_DRAWINFO{  
   UINT cbSize;  
   DWORD dwDrawAspect;  
   LONG lindex;  
   DVTARGETDEVICE* ptd;  
   HDC hicTargetDev;  
   HDC hdcDraw;  
   LPCRECTL prcBounds;  
   LPCRECTL prcWBounds;  
   BOOL bOptimize;  
   BOOL bZoomed;  
   BOOL bRectInHimetric;  
   SIZEL ZoomNum;  
   SIZEL ZoomDen;  
};  
```  
  
## Members  
 `cbSize`  
 The size of the structure, in bytes.  
  
 **dwDrawAspect**  
 Specifies how the target is to be represented. Representations can include content, an icon, a thumbnail, or a printed document. For a list of possible values, see [DVASPECT](http://msdn.microsoft.com/library/windows/desktop/ms690318) and [DVASPECT2](http://msdn.microsoft.com/library/windows/desktop/ms688644).  
  
 **lindex**  
 Portion of the target that is of interest for the draw operation. Its interpretation varies depending on the value in the **dwDrawAspect** member.  
  
 **ptd**  
 Pointer to a [DVTARGETDEVICE](http://msdn.microsoft.com/library/windows/desktop/ms686613) structure that enables drawing optimizations depending on the aspect specified. Note that newer objects and containers that support optimized drawing interfaces support this member as well. Older objects and containers that do not support optimized drawing interfaces always specify **NULL** for this member.  
  
 **hicTargetDev**  
 Information context for the target device pointed to by **ptd** from which the object can extract device metrics and test the device's capabilities. If **ptd** is **NULL**, the object should ignore the value in the **hicTargetDev** member.  
  
 **hdcDraw**  
 The device context on which to draw. For a windowless object, the **hdcDraw** member is in the `MM_TEXT` mapping mode with its logical coordinates matching the client coordinates of the containing window. In addition, the device context should be in the same state as the one normally passed by a `WM_PAINT` message.  
  
 **prcBounds**  
 Pointer to a [RECTL](http://msdn.microsoft.com/library/windows/desktop/dd162907) structure specifying the rectangle on **hdcDraw** and in which the object should be drawn. This member controls the positioning and stretching of the object. This member should be **NULL** to draw a windowless in-place active object. In every other situation, **NULL** is not a legal value and should result in an `E_INVALIDARG` error code. If the container passes a non-**NULL** value to a windowless object, the object should render the requested aspect into the specified device context and rectangle. A container can request this from a windowless object to render a second, non-active view of the object or to print the object.  
  
 **prcWBounds**  
 If **hdcDraw** is a metafile device context (see [GetDeviceCaps](http://msdn.microsoft.com/library/windows/desktop/dd144877) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]), this is a pointer to a **RECTL** structure specifying the bounding rectangle in the underlying metafile. The rectangle structure contains the window extent and window origin. These values are useful for drawing metafiles. The rectangle indicated by **prcBounds** is nested inside this **prcWBounds** rectangle; they are in the same coordinate space.  
  
 **bOptimize**  
 Nonzero if the drawing of the control is to be optimized, otherwise 0. If the drawing is optimized, the state of the device context is automatically restored when you are finished rendering.  
  
 **bZoomed**  
 Nonzero if the target has a zoom factor, otherwise 0. The zoom factor is stored in **ZoomNum**.  
  
 **bRectInHimetric**  
 Nonzero if the dimensions of **prcBounds** are in **HIMETRIC**, otherwise 0.  
  
 **ZoomNum**  
 The width and height of the rectangle into which the object is rendered. The zoom factor along the x-axis (the proportion of the object's natural size to its current extent) of the target is the value of **ZoomNum.cx** divided by the value of **ZoomDen.cx**. The zoom factor along the y-axis is achieved in a similar fashion.  
  
 **ZoomDen**  
 The actual width and height of the target.  
  
## Remarks  
 Typical usage of this structure would be the retrieval of information during the rendering of the target object. For example, you could retrieve values from `ATL_DRAWINFO` inside your overload of [CComControlBase::OnDrawAdvanced](../vs140/CComControlBase--OnDrawAdvanced.md).  
  
 This structure stores pertinent information used to render the appearance of an object for the target device. The information provided can be used in drawing to the screen, a printer, or even a metafile.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [Structures](../vs140/ATL-Structures.md)   
 [IViewObject::Draw](http://msdn.microsoft.com/library/windows/desktop/ms688655)   
 [CComControlBase::OnDrawAdvanced](../vs140/CComControlBase--OnDrawAdvanced.md)