---
title: "CHtmlView::OnUpdateUI"
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
ms.assetid: 9fc93894-d181-4d26-80c7-8b15bdef0262
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnUpdateUI
Notifies the host that the command state has changed.  
  
## Syntax  
  
```  
  
virtual HRESULT OnUpdateUI( );  
  
```  
  
## Return Value  
 `S_OK` if successful, or an OLE-defined error code otherwise.  
  
## Remarks  
 The host should update the state of toolbar buttons. This method is called regardless of the return value from `ShowUI`. Override `OnUpdateUI` to react to the `UpdateUI` notification from the Microsoft Web Browser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIHandler::UpdateUI](https://msdn.microsoft.com/en-us/library/aa753268.aspx)   
 [CHtmlView::OnShowUI](../vs140/CHtmlView--OnShowUI.md)   
 [CHtmlView::OnHideUI](../vs140/CHtmlView--OnHideUI.md)   
 [CHtmlView::OnShowContextMenu](../vs140/CHtmlView--OnShowContextMenu.md)