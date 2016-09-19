---
title: "CPaneDivider::GetPanes"
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
ms.assetid: cfb5ae22-2272-4b8b-b68f-74b463c4f5c1
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneDivider::GetPanes
Returns the list of panes that reside in the [CPaneContainer](../vs140/CPaneContainer-Class.md). This method should be called only to retrieve default pane dividers.  
  
## Syntax  
  
```  
void GetPanes(  
    CObList& lstBars   
);  
```  
  
#### Parameters  
 [out] `lstBars`  
 Contains the list of panes that reside in the pane container.  
  
## Remarks  
 This method should be called for default pane dividers only. A default pane divider is a divider that resizes the entire pane container.  
  
## Requirements  
 **Header:** afxPaneDivider.h  
  
## See Also  
 [CPaneDivider Class](../vs140/CPaneDivider-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)