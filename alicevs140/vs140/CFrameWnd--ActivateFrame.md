---
title: "CFrameWnd::ActivateFrame"
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
ms.assetid: 3abd3daf-1b21-46de-9919-f9161792519e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::ActivateFrame
Call this member function to activate and restore the frame window so that it is visible and available to the user.  
  
## Syntax  
  
```  
  
      virtual void ActivateFrame(  
   int nCmdShow = -1   
);  
```  
  
#### Parameters  
 `nCmdShow`  
 Specifies the parameter to pass to [CWnd::ShowWindow](../vs140/CWnd--ShowWindow.md). By default, the frame is shown and correctly restored.  
  
## Remarks  
 This member function is usually called after a non-user interface event such as a DDE, OLE, or other event that may show the frame window or its contents to the user.  
  
 The default implementation activates the frame and brings it to the top of the Z-order and, if necessary, carries out the same steps for the application's main frame window.  
  
 Override this member function to change how a frame is activated. For example, you can force MDI child windows to be maximized. Add the appropriate functionality, then call the base class version with an explicit `nCmdShow`.  
  
## Example  
 [!CODE [NVC_MFCWindowing#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#1)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)