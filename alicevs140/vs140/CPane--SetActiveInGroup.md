---
title: "CPane::SetActiveInGroup"
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
ms.assetid: 48b8bd81-6384-4658-bde5-ec40a22ccd00
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::SetActiveInGroup
Flags a pane as active.  
  
## Syntax  
  
```  
virtual void SetActiveInGroup(  
   BOOL bActive  
);  
```  
  
#### Parameters  
 [in] `bActive`  
 A `BOOL` that specifies whether the pane is flagged as active.  
  
## Remarks  
 When a dockable pane is shown or an auto-hide button is chosen, the corresponding auto-hide pane is marked as active.  
  
 The appearance of an auto-hide button that is associated with the pane is based on two factors. If the pane is active, and the `static``BOOL``CMFCAutoHideButton::m_bOverlappingTabs` is `TRUE`, the framework displays the auto-hide button as an icon and a label. For an inactive pane, the framework displays only the auto-hide icon.  
  
 If `CMFCAutoHideButton::m_bOverlappingTabs` is `FALSE`, or if the pane is not located in a group, the framework displays the associated auto-hide button as an icon and a label.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)