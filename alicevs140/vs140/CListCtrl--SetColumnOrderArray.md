---
title: "CListCtrl::SetColumnOrderArray"
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
ms.assetid: d408d643-b727-44bd-bcf3-5c44cd1dde2d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetColumnOrderArray
Sets the column order (left to right) of a list view control.  
  
## Syntax  
  
```  
  
      BOOL SetColumnOrderArray(  
   int iCount,  
   LPINT piArray   
);  
```  
  
#### Parameters  
 `piArray`  
 A pointer to a buffer containing the index values of the columns in the list view control (from left to right). The buffer must be large enough to contain the total number of columns in the list view control.  
  
 `iCount`  
 Number of columns in the list view control.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetColumnOrderArray](http://msdn.microsoft.com/library/windows/desktop/bb775072), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CListCtrl::GetColumnOrderArray](../vs140/CListCtrl--GetColumnOrderArray.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetColumnOrderArray](../vs140/CListCtrl--GetColumnOrderArray.md)