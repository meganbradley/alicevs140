---
title: "CListCtrl::GetGroupInfo"
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
ms.assetid: 3cc57d91-20b4-4e3d-9632-52b0b92c7329
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetGroupInfo
Gets the information for a specified group of the list view control.  
  
## Syntax  
  
```  
  
      int GetGroupInfo(  
   int iGroupId,  
   PLVGROUP pgrp   
) const;  
```  
  
#### Parameters  
 `iGroupId`  
 The identifier of the group whose information is to be retrieved.  
  
 `pgrp`  
 A pointer to the [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769) containing information on the group specified.  
  
## Return Value  
 Returns the ID of the group if successful, or -1 otherwise.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_GETGROUPINFO](http://msdn.microsoft.com/library/windows/desktop/bb774932) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetGroupInfo](../vs140/CListCtrl--SetGroupInfo.md)