---
title: "CMFCDesktopAlertWnd::OnClickLinkButton"
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
ms.assetid: b32df85c-6089-471a-83fe-27ef3f48357b
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDesktopAlertWnd::OnClickLinkButton
Called by the framework when the user clicks a link button located on the desktop alert menu.  
  
## Syntax  
  
```  
virtual BOOL OnClickLinkButton(  
    UINT uiCmdID  
);  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 This parameter is not used.  
  
## Return Value  
 Always `FALSE`.  
  
## Remarks  
 Override this method in a derived class if you want to be notified when a user clicks the link on the alert window.  
  
## Requirements  
 **Header:** afxDesktopAlertWnd.h  
  
## See Also  
 [CMFCDesktopAlertWnd Class](../vs140/CMFCDesktopAlertWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)