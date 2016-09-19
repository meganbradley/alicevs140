---
title: "CMFCAutoHideButton::IsActive"
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
ms.assetid: 2ca43f3a-4e30-4e41-93ba-f03c4acfe91c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAutoHideButton::IsActive
Indicates whether the auto-hide button is active.  
  
## Syntax  
  
```  
BOOL IsActive() const;  
```  
  
## Return Value  
 `TRUE` if the auto-hide button is active; `FALSE` otherwise.  
  
## Remarks  
 An auto-hide button is active when the associated [CDockablePane Class](../vs140/CDockablePane-Class.md) window is shown.  
  
## Requirements  
 **Header:** afxautohidebutton.h  
  
## See Also  
 [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)