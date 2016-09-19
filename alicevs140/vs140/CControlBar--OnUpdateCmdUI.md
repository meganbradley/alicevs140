---
title: "CControlBar::OnUpdateCmdUI"
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
ms.assetid: 0d7a5a01-626c-40ba-9766-858b3313dc44
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::OnUpdateCmdUI
This member function is called by the framework to update the status of the toolbar or status bar.  
  
## Syntax  
  
```  
  
      virtual void OnUpdateCmdUI(  
   CFrameWnd* pTarget,  
   BOOL bDisableIfNoHndler   
) = 0;  
```  
  
#### Parameters  
 `pTarget`  
 Points to the main frame window of the application. This pointer is used for routing update messages.  
  
 `bDisableIfNoHndler`  
 Flag that indicates whether a control that has no update handler should be automatically displayed as disabled.  
  
## Remarks  
 To update an individual button or pane, use the `ON_UPDATE_COMMAND_UI` macro in your message map to set an update handler appropriately. See [ON_UPDATE_COMMAND_UI](../vs140/ON_UPDATE_COMMAND_UI.md) for more information about using this macro.  
  
 `OnUpdateCmdUI` is called by the framework when the application is idle. The frame window to be updated must be a child window, at least indirectly, of a visible frame window. `OnUpdateCmdUI` is an advanced overridable.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [ON_UPDATE_COMMAND_UI](../vs140/ON_UPDATE_COMMAND_UI.md)   
 [TN031: Control Bars](../vs140/TN031--Control-Bars.md)