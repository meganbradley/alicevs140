---
title: "CDockablePane::DockPaneContainer"
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
ms.assetid: f49e2f2d-7e0d-4d60-b123-1033515a309f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::DockPaneContainer
Docks a container to the pane.  
  
## Syntax  
  
```  
virtual BOOL DockPaneContainer(  
   CPaneContainerManager& barContainerManager,  
   DWORD dwAlignment,  
   AFX_DOCK_METHOD dockMethod  
);  
```  
  
#### Parameters  
 [in] `barContainerManager`  
 A reference to the container manager of the container that is being docked.  
  
 [in] `dwAlignment`  
 `DWORD` that specifies the side of the pane to which the container is being docked.  
  
 [in] `dockMethod`  
 Not used.  
  
## Return Value  
 `TRUE` if the container was successfully docked to the pane; otherwise, `FALSE`.  
  
## Remarks  
 `dwAlignment` can be any of the following values:  
  
|Value|Description|  
|-----------|-----------------|  
|`CBRS_ALIGN_TOP`|The container is being docked to the top of the pane.|  
|`CBRS_ALIGN_BOTTOM`|The container is being docked to the bottom of the pane.|  
|`CBRS_ALIGN_LEFT`|The container is being docked to the left of the pane.|  
|`CBRS_ALIGN_RIGHT`|The container is being docked to the right of the pane.|  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPaneContainerManager Class](../vs140/CPaneContainerManager-Class.md)