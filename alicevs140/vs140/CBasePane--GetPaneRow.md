---
title: "CBasePane::GetPaneRow"
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
ms.assetid: c764dd6a-5312-4319-9be5-97fcfcd88826
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::GetPaneRow
Returns a pointer to the [CDockingPanesRow](../vs140/CDockingPanesRow-Class.md)object where the pane is docked.  
  
## Syntax  
  
```  
CDockingPanesRow* GetPaneRow();  
```  
  
## Return Value  
 A pointer to `CDockingPanesRow` if the pane is docked, or `NULL` if it is floating.  
  
## Remarks  
 Call this method to access the row where a pane is docked. For example, to arrange the panes in a particular row, call `GetPaneRow` and then call [CDockingPanesRow::ArrangePanes](../vs140/CDockingPanesRow--ArrangePanes.md).  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)