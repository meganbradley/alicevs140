---
title: "CMFCTabCtrl::SetActiveInMDITabGroup"
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
ms.assetid: b135d9f5-a8ea-4ab7-adb7-a0326098310c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::SetActiveInMDITabGroup
Sets the current tab of a tab control as the active tab in a multiple document interface tab group.  
  
## Syntax  
  
```  
void SetActiveInMDITabGroup(  
   BOOL bActive  
);  
```  
  
#### Parameters  
 [in] `bActive`  
 `TRUE` to make the current tab the active tab; `FALSE` to make the current tab inactive.  
  
## Remarks  
 You can organize multiple document windows into either vertical or horizontal tab groups and easily shuffle documents from one tab group to another.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCTabCtrl::IsActiveInMDITabGroup](../vs140/CMFCTabCtrl--IsActiveInMDITabGroup.md)   
 [Window Types](../vs140/Kinds-of-Windows.md)   
 [Managing MDI Child Windows](../vs140/Managing-MDI-Child-Windows.md)