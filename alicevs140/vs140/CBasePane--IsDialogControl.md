---
title: "CBasePane::IsDialogControl"
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
ms.assetid: 5e07784e-7c3f-4c17-9ab0-4fcf600c0bef
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::IsDialogControl
Specifies whether the pane is a dialog box control.  
  
## Syntax  
  
```  
BOOL IsDialogControl() const;  
```  
  
## Return Value  
 `TRUE` if the pane is a dialog box control; otherwise, `FALSE`.  
  
## Remarks  
 The framework uses this method to ensure layout consistency for all panes.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)