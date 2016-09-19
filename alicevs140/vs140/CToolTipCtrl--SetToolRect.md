---
title: "CToolTipCtrl::SetToolRect"
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
ms.assetid: f0c038cb-ebc5-4a12-9a04-5a2480d2971f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::SetToolRect
Sets a new bounding rectangle for a tool.  
  
## Syntax  
  
```  
  
      void SetToolRect(  
   CWnd* pWnd,  
   UINT_PTR nIDTool,  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `pWnd`  
 Pointer to the window that contains the tool.  
  
 `nIDTool`  
 ID of the tool.  
  
 `lpRect`  
 Pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure specifying the new bounding rectangle.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::GetToolInfo](../vs140/CToolTipCtrl--GetToolInfo.md)