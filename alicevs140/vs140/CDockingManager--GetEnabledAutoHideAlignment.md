---
title: "CDockingManager::GetEnabledAutoHideAlignment"
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
ms.assetid: 039f6674-0049-431a-9277-dcdc2b671b70
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::GetEnabledAutoHideAlignment
Returns the enabled alignment of the panes.  
  
## Syntax  
  
```  
DWORD GetEnabledAutoHideAlignment() const;  
```  
  
## Return Value  
 A bitwise combination of `CBRS_ALIGN_` flags, or 0 if autohide panes are not enabled. For more information, see [CFrameWnd::EnableDocking](../vs140/CFrameWnd--EnableDocking.md).  
  
## Remarks  
 The method returns the enabled alignment for autohide control bars. To enable autohide bars, call [CFrameWndEx::EnableAutoHidePanes](../vs140/CFrameWndEx--EnableAutoHidePanes.md).  
  
## Requirements  
 **Header:** afxDockingManager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)