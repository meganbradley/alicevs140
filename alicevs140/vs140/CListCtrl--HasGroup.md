---
title: "CListCtrl::HasGroup"
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
ms.assetid: 6d8de8ef-5227-447b-b8f2-ef911a332b35
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::HasGroup
Determines if the list view control has the specified group.  
  
## Syntax  
  
```  
  
      BOOL HasGroup(  
   int iGroupId   
) const;  
```  
  
#### Parameters  
 `iGroupId`  
 The identifier of the group being requested.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_HASGROUP](http://msdn.microsoft.com/library/windows/desktop/bb761097) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)