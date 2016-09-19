---
title: "CListCtrl::GetSelectedColumn"
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
ms.assetid: 539e0869-a767-4d47-9235-6fb5b2f4eec8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetSelectedColumn
Retrieves the index of the currently-selected column in the list control.  
  
## Syntax  
  
```  
  
UINT GetSelectedColumn( ) const;  
  
```  
  
## Return Value  
 The index of the selected column.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_GETSELECTEDCOLUMN](http://msdn.microsoft.com/library/windows/desktop/bb761067) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl::SetSelectedColumn](../vs140/CListCtrl--SetSelectedColumn.md)   
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)