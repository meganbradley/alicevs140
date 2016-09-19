---
title: "IOleObjectImpl::DoVerbInPlaceActivate"
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
ms.assetid: 5b24835d-967c-4139-beb5-18782bd783c6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::DoVerbInPlaceActivate
Runs the control and installs its window, but does not install the control's user interface.  
  
## Syntax  
  
```  
  
      HRESULT DoVerbInPlaceActivate(  
   LPCRECT prcPosRect,  
   HWND /* hwndParent */  
);  
```  
  
#### Parameters  
 `prcPosRec`  
 [in] Pointer to the rectangle the container wants the control to draw into.  
  
 *hwndParent*  
 [in] Handle of the window containing the control. Not used in the ATL implementation.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 Activates the control in place by calling [CComControlBase::InPlaceActivate](../vs140/CComControlBase--InPlaceActivate.md). Unless the control class's data member `m_bWindowOnly` is **TRUE**, `DoVerbInPlaceActivate` first attempts to activate the control as a windowless control (possible only if the container supports [IOleInPlaceSiteWindowless](http://msdn.microsoft.com/library/windows/desktop/ms682300)). If that fails, the function attempts to activate the control with extended features (possible only if the container supports [IOleInPlaceSiteEx](http://msdn.microsoft.com/library/windows/desktop/ms693461)). If that fails, the function attempts to activate the control with no extended features (possible only if the container supports [IOleInPlaceSite](http://msdn.microsoft.com/library/windows/desktop/ms686586)). If activation succeeds, the function notifies the container the control has been activated.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [CComControlBase::InPlaceActivate](../vs140/CComControlBase--InPlaceActivate.md)   
 [CComControlBase::m_bWindowOnly](../vs140/CComControlBase--m_bWindowOnly.md)