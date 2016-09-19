---
title: "CToolTipCtrl::DelTool"
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
ms.assetid: 46af3e49-6a99-467b-b76f-1f2af808109c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::DelTool
Removes the tool specified by `pWnd` and `nIDTool` from the collection of tools supported by a tool tip control.  
  
## Syntax  
  
```  
  
      void DelTool(  
   CWnd* pWnd,  
   UINT_PTR nIDTool = 0   
);  
```  
  
#### Parameters  
 `pWnd`  
 Pointer to the window that contains the tool.  
  
 `nIDTool`  
 ID of the tool.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::AddTool](../vs140/CToolTipCtrl--AddTool.md)