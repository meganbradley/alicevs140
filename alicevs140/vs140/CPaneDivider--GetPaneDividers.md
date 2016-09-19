---
title: "CPaneDivider::GetPaneDividers"
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
ms.assetid: 99bb0e1b-9050-41e4-a425-bef753ec2fb2
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneDivider::GetPaneDividers
Returns the list of pane dividers that reside in the [CPaneContainer](../vs140/CPaneContainer-Class.md). This method should be called only for default pane dividers.  
  
## Syntax  
  
```  
void GetPaneDividers(  
    CObList& lstSliders   
);  
```  
  
#### Parameters  
 [out] `lstSliders`  
 Contains the list of pane dividers that reside in the pane container.  
  
## Remarks  
 This method should be called for default pane dividers only. A default pane divider is a divider that resizes the entire pane container.  
  
## Requirements  
 **Header:** afxPaneDivider.h  
  
## See Also  
 [CPaneDivider Class](../vs140/CPaneDivider-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)