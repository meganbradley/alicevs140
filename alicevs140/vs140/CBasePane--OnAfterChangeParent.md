---
title: "CBasePane::OnAfterChangeParent"
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
ms.assetid: 062f14d6-f955-4659-acf0-74207540277f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::OnAfterChangeParent
Called by the framework after the pane's parent changes.  
  
## Syntax  
  
```  
virtual void OnAfterChangeParent(  
   CWnd* pWndOldParent  
);  
```  
  
#### Parameters  
 [in] `pWndOldParent`  
 A pointer to the previous parent.  
  
## Remarks  
 The framework calls this method after the pane's parent changes, usually because of a docking or floating operation.  
  
 The default implementation does nothing.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)