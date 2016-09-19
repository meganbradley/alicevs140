---
title: "CToolTipCtrl::UpdateTipText"
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
ms.assetid: 0fc315b5-cb8b-40d3-97d5-b2eb16f62f46
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::UpdateTipText
Updates the tool tip text for this control's tools.  
  
## Syntax  
  
```  
  
      void UpdateTipText(  
   LPCTSTR lpszText,  
   CWnd* pWnd,  
   UINT_PTR nIDTool = 0   
);  
void UpdateTipText(  
   UINT nIDText,  
   CWnd* pWnd,  
   UINT_PTR nIDTool = 0   
);  
```  
  
#### Parameters  
 `lpszText`  
 Pointer to the text for the tool.  
  
 `pWnd`  
 Pointer to the window that contains the tool.  
  
 `nIDTool`  
 ID of the tool.  
  
 `nIDText`  
 ID of the string resource that contains the text for the tool.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::GetToolInfo](../vs140/CToolTipCtrl--GetToolInfo.md)