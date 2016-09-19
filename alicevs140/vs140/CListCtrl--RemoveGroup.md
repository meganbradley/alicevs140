---
title: "CListCtrl::RemoveGroup"
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
ms.assetid: 13623790-983a-4dee-93f4-7c3d42a36ff2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::RemoveGroup
Removes the specified group from the list view control.  
  
## Syntax  
  
```  
  
      LRESULT RemoveGroup(  
   int iGroupId   
);  
```  
  
#### Parameters  
 `iGroupId`  
 The identifier of the group to be removed.  
  
## Return Value  
 Returns the index of the group if successful, or -1 otherwise.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_REMOVEGROUP](http://msdn.microsoft.com/library/windows/desktop/bb761149) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)