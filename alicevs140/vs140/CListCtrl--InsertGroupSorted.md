---
title: "CListCtrl::InsertGroupSorted"
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
ms.assetid: fe20025a-52bc-4e71-bbf8-27dcb577c0ae
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::InsertGroupSorted
Inserts the specified group into an ordered list of groups.  
  
## Syntax  
  
```  
  
      LRESULT InsertGroupSorted(  
   PLVINSERTGROUPSORTED pStructInsert   
);  
```  
  
#### Parameters  
 *pStructInsert*  
 A pointer to an [LVINSERTGROUPSORTED](http://msdn.microsoft.com/library/windows/desktop/bb774756) structure that contains the group to insert.  
  
## Return Value  
 The return value is not used.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_INSERTGROUPSORTED](http://msdn.microsoft.com/library/windows/desktop/bb761105) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)