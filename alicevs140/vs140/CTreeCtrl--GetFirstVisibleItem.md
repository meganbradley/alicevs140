---
title: "CTreeCtrl::GetFirstVisibleItem"
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
ms.assetid: 80158753-c000-43ac-867b-9d5a25ee9a0d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetFirstVisibleItem
Call this function to retrieve the first visible item of the tree view control.  
  
## Syntax  
  
```  
  
HTREEITEM GetFirstVisibleItem( ) const;  
```  
  
## Return Value  
 The handle of the first visible item; otherwise **NULL**.  
  
## Example  
 See the example for [CTreeCtrl::SetCheck](../vs140/CTreeCtrl--SetCheck.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetNextVisibleItem](../vs140/CTreeCtrl--GetNextVisibleItem.md)   
 [CTreeCtrl::GetPrevVisibleItem](../vs140/CTreeCtrl--GetPrevVisibleItem.md)   
 [CTreeCtrl::EnsureVisible](../vs140/CTreeCtrl--EnsureVisible.md)   
 [CTreeCtrl::GetVisibleCount](../vs140/CTreeCtrl--GetVisibleCount.md)