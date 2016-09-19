---
title: "CBaseTabbedPane::FindBarByTabNumber"
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
ms.assetid: fb0ca90b-7b77-434a-bf83-d4cfcd3d05b9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTabbedPane::FindBarByTabNumber
Returns a pane that resides in a tab.  
  
## Syntax  
  
```  
virtual CWnd* FindBarByTabNumber(  
    int nTabNum,  
    BOOL bGetWrappedBar = FALSE  
);  
```  
  
#### Parameters  
 [in] `nTabNum`  
 Specifies the zero-based index of the tab to retrieve.  
  
 [in] `bGetWrappedBar`  
 `TRUE` to return the underlying (wrapped) window of the pane instead of the pane itself; otherwise `FALSE`. This only applies to panes derived from [CDockablePaneAdapter](../vs140/CDockablePaneAdapter-Class.md).  
  
## Return Value  
 If the pane is found, then a valid pointer to the pane being searched for is returned; otherwise, `NULL`.  
  
## Remarks  
 Call this method to retrieve the pane residing in the tab specified by the `nTabNum` parameter.  
  
## Requirements  
 **Header:** afxBaseTabbedPane.h  
  
## See Also  
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)