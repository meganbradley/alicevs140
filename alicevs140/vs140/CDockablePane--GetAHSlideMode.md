---
title: "CDockablePane::GetAHSlideMode"
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
ms.assetid: 8b6b9038-d543-4676-8202-06bf95c84b80
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::GetAHSlideMode
Retrieves the auto-hide slide mode for the pane.  
  
## Syntax  
  
```  
virtual UINT GetAHSlideMode() const;  
```  
  
## Return Value  
 A `UINT` that specifies the auto-hide slide mode for the pane. The return value can be either `AFX_AHSM_MOVE` or `AFX_AHSM_STRETCH`, but the implementation only uses `AFX_AHSM_MOVE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)