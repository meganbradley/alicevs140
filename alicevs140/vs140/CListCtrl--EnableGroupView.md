---
title: "CListCtrl::EnableGroupView"
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
ms.assetid: db7cac3d-f429-4e8f-8006-1debc044bde3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::EnableGroupView
Enables or disables whether the items in a list view control display as a group.  
  
## Syntax  
  
```  
  
      LRESULT EnableGroupView(  
   BOOL fEnable   
);  
```  
  
#### Parameters  
 `fEnable`  
 Indicates whether to enable a listview control to group displayed items. **TRUE** to enable grouping; **FALSE** to disable it.  
  
## Return Value  
 Returns one of the following values:  
  
-   **0** The ability to display list view items as a group is already enabled or disabled.  
  
-   **1** The state of the control was successfully changed.  
  
-   **-1** The operation failed.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_ENABLEGROUPVIEW](http://msdn.microsoft.com/library/windows/desktop/bb774900) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)