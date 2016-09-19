---
title: "CHtmlView::OnHideUI"
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
ms.assetid: a0a407d1-2df9-47d0-9c94-e6129d9aa893
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnHideUI
This member function is called by the framework when Internet Explorer or MSHTML removes its menus and toolbars.  
  
## Syntax  
  
```  
  
virtual HRESULT OnHideUI( );  
  
```  
  
## Return Value  
 `S_OK` if successful, or an OLE-defined error code otherwise.  
  
## Remarks  
 Override `OnHideUI` to react to the `HideUI` notification from the Microsoft Web Browser control. See [IDocHostUIHandler::HideUI](https://msdn.microsoft.com/en-us/library/aa753259.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::OnUpdateUI](../vs140/CHtmlView--OnUpdateUI.md)   
 [CHtmlView::OnShowUI](../vs140/CHtmlView--OnShowUI.md)   
 [CHtmlView::OnShowContextMenu](../vs140/CHtmlView--OnShowContextMenu.md)