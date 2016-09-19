---
title: "CListCtrl::MoveGroup"
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
ms.assetid: 4162c14d-4d0c-47e0-ac60-e861ab6d48f2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::MoveGroup
Moves the specified group to the specified zero based index of the list view control.  
  
## Syntax  
  
```  
  
      LRESULT MoveGroup(  
   int iGroupId,  
   int toIndex   
);  
```  
  
#### Parameters  
 `iGroupId`  
 The identifier of the group to be moved.  
  
 `toIndex`  
 The zero-based index where the group is to be moved.  
  
## Return Value  
 The return value is not used.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_MOVEGROUP](http://msdn.microsoft.com/library/windows/desktop/bb761141) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)