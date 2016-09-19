---
title: "CBasePane::HideInPrintPreviewMode"
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
ms.assetid: a602c168-9694-4782-a66e-40da5778bb05
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::HideInPrintPreviewMode
Specifies whether the pane is hidden in print preview.  
  
## Syntax  
  
```  
virtual BOOL HideInPrintPreviewMode() const;  
```  
  
## Return Value  
 `TRUE` if the pane is not shown in print preview; otherwise, `FALSE`.  
  
## Remarks  
 Base panes are not shown in print preview. Therefore, this method always returns `TRUE`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)