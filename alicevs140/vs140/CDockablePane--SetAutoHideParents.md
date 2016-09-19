---
title: "CDockablePane::SetAutoHideParents"
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
ms.assetid: 97f3a394-dcff-4173-af78-32479eb14504
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::SetAutoHideParents
Sets the auto-hide button and auto-hide toolbar for the pane.  
  
## Syntax  
  
```  
void SetAutoHideParents(  
   CMFCAutoHideBar* pToolBar,  
   CMFCAutoHideButton* pBtn  
);  
```  
  
#### Parameters  
 [in] `pToolBar`  
 Pointer to an auto-hide toolbar.  
  
 [in] `pBtn`  
 Pointer to an auto-hide button.  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCAutoHideBar Class](../vs140/CMFCAutoHideBar-Class.md)   
 [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md)