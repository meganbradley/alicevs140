---
title: "CWnd::UpdateDialogControls"
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
ms.assetid: 9418dac3-6e84-4355-ac06-661fa32f7e6e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::UpdateDialogControls
Call this member function to update the state of dialog buttons and other controls in a dialog box or window that uses the [ON_UPDATE_COMMAND_UI](../vs140/ON_UPDATE_COMMAND_UI.md) callback mechanism.  
  
## Syntax  
  
```  
  
      void UpdateDialogControls(  
   CCmdTarget* pTarget,  
   BOOL bDisableIfNoHndler   
);  
```  
  
#### Parameters  
 `pTarget`  
 Points to the main frame window of the application, and is used for routing update messages*.*  
  
 `bDisableIfNoHndler`  
 Flag that indicates whether a control that has no update handler should be automatically displayed as disabled.  
  
## Remarks  
 If a child control does not have a handler and `bDisableIfNoHndler` is **TRUE**, then the child control will be disabled.  
  
 The framework calls this member function for controls in dialog bars or toolbars as part of the application's idle processing.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::m_bAutoMenuEnable](../vs140/CFrameWnd--m_bAutoMenuEnable.md)