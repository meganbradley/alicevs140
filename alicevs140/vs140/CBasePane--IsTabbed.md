---
title: "CBasePane::IsTabbed"
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
ms.assetid: 9387323d-dbff-48a5-bc7f-2056deb4f003
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::IsTabbed
Determines whether the pane has been inserted in the tab control of a tabbed window.  
  
## Syntax  
  
```  
virtual BOOL IsTabbed() const;  
```  
  
## Return Value  
 `TRUE` if the control bar is inserted in a tab of a tabbed window; otherwise `FALSE`.  
  
## Remarks  
 This method retrieves a pointer to the immediate parent and determines if the parent's runtime class is [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md).  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)