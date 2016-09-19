---
title: "CDockablePane::GetDefaultPaneDivider"
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
ms.assetid: 71e00fbb-9840-4c55-ac47-137cd928d8ac
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::GetDefaultPaneDivider
Returns the default pane divider for the pane's container.  
  
## Syntax  
  
```  
CPaneDivider* GetDefaultPaneDivider() const;  
```  
  
## Return Value  
 A valid [CPaneDivider](../vs140/CPaneDivider-Class.md) object if the dockable pane is docked to the main frame window, or `NULL` if the dockable pane is not docked or if it is floating.  
  
## Remarks  
 For more information about pane dividers, see [CPaneDivider Class](../vs140/CPaneDivider-Class.md).  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)