---
title: "CListCtrl::GetFocusedGroup"
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
ms.assetid: 280e6ebb-f96b-41ab-afe5-8f3126c62618
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetFocusedGroup
Retrieves the group that has the keyboard focus in the current list-view control.  
  
## Syntax  
  
```  
int GetFocusedGroup() const;  
```  
  
## Return Value  
 The index of the group whose state is `LVGS_FOCUSED`, if there is such a group; otherwise, -1.  
  
## Remarks  
 This method sends the [LVM_GETFOCUSEDGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774925) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For more information, see the `LVGS_FOCUSED` value of the `state` member of the [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769) structure.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LVM_GETFOCUSEDGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774925)   
 [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769)