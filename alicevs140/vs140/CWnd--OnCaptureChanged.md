---
title: "CWnd::OnCaptureChanged"
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
ms.assetid: e968d2c8-d887-49d0-8245-3a335706511a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnCaptureChanged
The framework calls this member function to notify the window that is losing the mouse capture.  
  
## Syntax  
  
```  
  
      afx_msg void OnCaptureChanged(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 A pointer to the window to gain mouse capture  
  
## Remarks  
 A window receives this message even if it calls [ReleaseCapture](http://msdn.microsoft.com/library/windows/desktop/ms646261) itself. An application should not attempt to set the mouse capture in response to this message. When it receives this message, a window should redraw itself, if necessary, to reflect the new mouse-capture state.  
  
 See the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for information on the `ReleaseCapture` Windows function.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_CAPTURECHANGED](http://msdn.microsoft.com/library/windows/desktop/ms645605)