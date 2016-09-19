---
title: "CDockablePane::CopyState"
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
ms.assetid: 0c327a03-0232-41a3-8483-8c5f2b328c05
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::CopyState
Copies the state of a dockable pane.  
  
## Syntax  
  
```  
virtual void CopyState(  
   CDockablePane* pOrgBar  
);  
```  
  
#### Parameters  
 [in] `pOrgBar`  
 A pointer to a dockable pane.  
  
## Remarks  
 `CDockablePane::CopyState` copies the state of `pOrgBar` to the current pane by calling the following methods:  
  
-   [CPane::CopyState](../vs140/CPane--CopyState.md)  
  
-   [CDockablePane::GetAHRestoredRect](../vs140/CDockablePane--GetAHRestoredRect.md)  
  
-   [CDockablePane::GetAHSlideMode](../vs140/CDockablePane--GetAHSlideMode.md)  
  
-   [CDockablePane::GetLastPercentInPaneContainer](../vs140/CDockablePane--GetLastPercentInPaneContainer.md)  
  
-   [CDockablePane::IsAutohideAllEnabled](../vs140/CDockablePane--IsAutohideAllEnabled.md)  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)