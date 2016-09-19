---
title: "CSplitterWnd::CreateScrollBarCtrl"
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
ms.assetid: 6e71c855-c9d6-4372-a927-155bce4236f2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::CreateScrollBarCtrl
Called by the framework to create a shared scroll bar control.  
  
## Syntax  
  
```  
  
      virtual BOOL CreateScrollBarCtrl(  
   DWORD dwStyle,  
   UINT nID   
);  
```  
  
#### Parameters  
 `dwStyle`  
 Specifies the window style.  
  
 `nID`  
 The child window ID of the window. The ID can be **AFX_IDW_PANE_FIRST** unless the splitter window is nested inside another splitter window.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Override `CreateScrollBarCtrl` to include extra controls next to a scroll bar. The default behavior is to create normal Windows scroll bar controls.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [AfxGetInstanceHandle](../vs140/AfxGetInstanceHandle.md)