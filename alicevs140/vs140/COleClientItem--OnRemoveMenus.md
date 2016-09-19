---
title: "COleClientItem::OnRemoveMenus"
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
ms.assetid: 3229aa10-7cdb-42b6-b69c-5282d0792344
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnRemoveMenus
Called by the framework to remove the container's menus from the specified composite menu when in-place activation ends.  
  
## Syntax  
  
```  
  
      virtual void OnRemoveMenus(  
   CMenu* pMenuShared   
);  
```  
  
#### Parameters  
 `pMenuShared`  
 Points to the composite menu constructed by calls to the [OnInsertMenus](../vs140/COleClientItem--OnInsertMenus.md) member function.  
  
## Remarks  
 The default implementation removes from `pMenuShared` the in-place container menus, that is, the File, Container, and Window menu groups. Override this function if the default implementation is not appropriate for your application; for example, if your application does not use document templates for associating resources with document types. If you override this function, you should probably override [OnInsertMenus](../vs140/COleClientItem--OnInsertMenus.md) and [OnSetMenu](../vs140/COleClientItem--OnSetMenu.md) as well. This is an advanced overridable.  
  
 The submenus on `pMenuShared` may be shared by more than one composite menu if the server has repeatedly called `OnInsertMenus`. Therefore you should not delete any submenus in your override of `OnRemoveMenus`; you should only detach them.  
  
 For more information, see [IOleInPlaceFrame::RemoveMenus](http://msdn.microsoft.com/library/windows/desktop/ms688685) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnInsertMenus](../vs140/COleClientItem--OnInsertMenus.md)   
 [COleClientItem::OnSetMenu](../vs140/COleClientItem--OnSetMenu.md)