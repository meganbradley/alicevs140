---
title: "IOleInPlaceObjectWindowlessImpl::SetObjectRects"
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
ms.assetid: 306dd357-1d51-48f4-9cab-2d07b3a440e7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceObjectWindowlessImpl::SetObjectRects
Called by the container to inform the control that its size and/or position has changed.  
  
## Syntax  
  
```  
  
      HRESULT SetObjectRects(  
   LPCRECT prcPos,  
   LPCRECT prcClip   
);  
```  
  
## Remarks  
 Updates the control's `m_rcPos` data member and the control display. Only the part of the control that intersects the clip region is displayed. If a control's display was previously clipped but the clipping has been removed, this function can be called to redraw a full view of the control.  
  
 See [IOleInPlaceObject::SetObjectRects](http://msdn.microsoft.com/library/windows/desktop/ms683767) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleInPlaceObjectWindowlessImpl Class](../vs140/IOleInPlaceObjectWindowlessImpl-Class.md)   
 [CComControlBase::m_rcPos](../vs140/CComControlBase--m_rcPos.md)