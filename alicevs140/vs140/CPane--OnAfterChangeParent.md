---
title: "CPane::OnAfterChangeParent"
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
ms.assetid: 225219d1-efe8-4d47-9a41-9e53ea27f3e0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::OnAfterChangeParent
Called by the framework when the parent of a pane has changed.  
  
## Syntax  
  
```  
virtual void OnAfterChangeParent(  
    CWnd* pWndOldParent  
);  
```  
  
#### Parameters  
 [in] [out] `pWndOldParent`  
 The pane's previous parent window.  
  
## Remarks  
 This method is called by the framework when the parent of a pane has changed because of a docking or floating operation.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)