---
title: "CPane::OnBeforeChangeParent"
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
ms.assetid: e143bf50-a0fe-48cd-afeb-18a61de1b75b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::OnBeforeChangeParent
Called by the framework when the parent of the pane is about to change.  
  
## Syntax  
  
```  
virtual void OnBeforeChangeParent(  
    CWnd* pWndNewParent,  
    BOOL bDelay = FALSE  
);  
```  
  
#### Parameters  
 [in] [out] `pWndNewParent`  
 Specifies the new parent window.  
  
 [in] `bDelay`  
 `TRUE` to delay the global docking layout adjustment; otherwise, `FALSE`.  
  
## Remarks  
 This method is called by the framework when the parent of the pane is about to change because the pane is being docked or floated.  
  
 By default, the pane is unregistered with the docking pane by calling `CDockSite::RemovePane`.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDockSite Class](../vs140/CDockSite-Class.md)