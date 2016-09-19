---
title: "IOleInPlaceObjectWindowlessImpl::InPlaceDeactivate"
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
ms.assetid: ed96e29d-39a1-4274-85db-d73a5bf690ca
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceObjectWindowlessImpl::InPlaceDeactivate
Called by the container to deactivate an in-place active control.  
  
## Syntax  
  
```  
  
      HRESULT InPlaceDeactivate(  
   HWND* phwnd   
);  
```  
  
## Remarks  
 This method performs a full or partial deactivation depending on the state of the control. If necessary, the control's user interface is deactivated, and the control's window, if any, is destroyed. The container is notified that the control is no longer active in place. The **IOleInPlaceUIWindow** interface used by the container to negotiate menus and border space is released.  
  
 See [IOleInPlaceObject::InPlaceDeactivate](http://msdn.microsoft.com/library/windows/desktop/ms679700) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleInPlaceObjectWindowlessImpl Class](../vs140/IOleInPlaceObjectWindowlessImpl-Class.md)   
 [CComControlBase::InPlaceActivate](../vs140/CComControlBase--InPlaceActivate.md)