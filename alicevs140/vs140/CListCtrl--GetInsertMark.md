---
title: "CListCtrl::GetInsertMark"
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
ms.assetid: ef7f527e-9bdc-4ed7-a03e-d7164c0bd99c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetInsertMark
Retrieves the current position of the insertion mark.  
  
## Syntax  
  
```  
  
      BOOL GetInsertMark(  
   LPLVINSERTMARK lvim   
) const;  
```  
  
#### Parameters  
 `lvim`  
 A pointer to an [LVINSERTMARK](http://msdn.microsoft.com/library/windows/desktop/bb774758) structure containing the information for the insert mark.  
  
## Return Value  
 Returns **TRUE** if successful, or **FALSE** otherwise. **FALSE** is returned if the size in the `cbSize` member of the **LVINSERTMARK** structure does not equal the actual size of the structure.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_GETINSERTMARK](http://msdn.microsoft.com/library/windows/desktop/bb774945) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)