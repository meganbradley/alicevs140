---
title: "CHtmlView::OnShowUI"
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
ms.assetid: 2b45aaeb-7dc4-4c5c-bf6b-e7d07a7e6555
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnShowUI
Called before Internet Explorer or MSHTML displays its menus and toolbars.  
  
## Syntax  
  
```  
  
      virtual HRESULT OnShowUI(  
   DWORD dwID,  
   LPOLEINPLACEACTIVEOBJECT pActiveObject,  
   LPOLECOMMANDTARGET pCommandTarget,  
   LPOLEINPLACEFRAME pFrame,  
   LPOLEINPLACEUIWINDOW pDoc   
);  
```  
  
#### Parameters  
 `dwID`  
 Reserved for future use.  
  
 `pActiveObject`  
 [IOleInPlaceActiveObject](http://msdn.microsoft.com/library/windows/desktop/ms691299) interface of the currently active object.  
  
 `pCommandTarget`  
 [IOleCommandTarget](http://msdn.microsoft.com/library/windows/desktop/ms683797) interface of the object.  
  
 `pFrame`  
 [IOleInPlaceFrame](http://msdn.microsoft.com/library/windows/desktop/ms692770) interface of the object. This is needed for menus and toolbars.  
  
 `pDoc`  
 [IOleInPlaceUIWindow](http://msdn.microsoft.com/library/windows/desktop/ms680716) interface for the object. This is needed for toolbars.  
  
## Return Value  
 See [IDocHostUIHandler::ShowUI](https://msdn.microsoft.com/en-us/library/aa753265.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a list of values.  
  
## Remarks  
 Override `OnShowUI` to react to the `ShowUI` notification from the Microsoft Web Browser control. See [IDocHostUIHandler::ShowUI](https://msdn.microsoft.com/en-us/library/aa753265.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::OnUpdateUI](../vs140/CHtmlView--OnUpdateUI.md)   
 [CHtmlView::OnHideUI](../vs140/CHtmlView--OnHideUI.md)   
 [CHtmlView::OnShowContextMenu](../vs140/CHtmlView--OnShowContextMenu.md)