---
title: "CBaseTabbedPane::FloatTab"
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
ms.assetid: 3c7038c3-db56-407e-a0e9-b7c1890235b2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTabbedPane::FloatTab
Floats a pane, but only if the pane currently resides in a detachable tab.  
  
## Syntax  
  
```  
virtual BOOL FloatTab(  
    CWnd* pBar,  
    int nTabID,  
    AFX_DOCK_METHOD dockMethod,  
    BOOL bHide = FALSE  
);  
```  
  
#### Parameters  
 [in] [out] `pBar`  
 A pointer to the pane to float.  
  
 [in] `nTabID`  
 Specifies the zero-based index of the tab to float.  
  
 [in] `dockMethod`  
 Specifies the method to use to make the pane float. For more information, see the Remarks section.  
  
 [in] `bHide`  
 `TRUE` to hide the pane before floating; otherwise, `FALSE`.  
  
## Return Value  
 `TRUE` if the pane floated; otherwise, `FALSE`.  
  
## Remarks  
 Call this method to float a pane that currently resides in a detachable tab.  
  
 If you want to detach a pane programmatically, specify `DM_SHOW` for the `dockMethod` parameter. If you want to float the pane in the same position where it floated previously, specify `DM_DBL_CLICK` as the `dockMethod` parameter.  
  
## Requirements  
 **Header:** afxBaseTabbedPane.h  
  
## See Also  
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)