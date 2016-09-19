---
title: "CDockingManager::m_bHideDockingBarsInContainerMode"
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
ms.assetid: 50f5c7ce-2f73-4146-a828-103cf8032733
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::m_bHideDockingBarsInContainerMode
Specifies whether the docking manager hides panes in OLE container mode.  
  
## Syntax  
  
```  
AFX_IMPORT_DATA static BOOL m_bHideDockingBarsInContainerMode;  
```  
  
## Remarks  
 Set this value to `FALSE` if you want to keep all panes docked to the main frame visible when the application is in OLE container mode. By default, this value is `TRUE`.  
  
## Requirements  
 **Header:** afxDockingManager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)