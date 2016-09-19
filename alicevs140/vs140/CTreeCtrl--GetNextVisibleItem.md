---
title: "CTreeCtrl::GetNextVisibleItem"
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
ms.assetid: 419a0e2d-af13-4b2d-8d5f-76575b129cc4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetNextVisibleItem
Call this function to retrieve the next visible item of `hItem`.  
  
## Syntax  
  
```  
  
      HTREEITEM GetNextVisibleItem(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
## Return Value  
 The handle of the next visible item; otherwise **NULL**.  
  
## Example  
 See the example for [CTreeCtrl::SetCheck](../vs140/CTreeCtrl--SetCheck.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetPrevVisibleItem](../vs140/CTreeCtrl--GetPrevVisibleItem.md)   
 [CTreeCtrl::GetFirstVisibleItem](../vs140/CTreeCtrl--GetFirstVisibleItem.md)   
 [CTreeCtrl::EnsureVisible](../vs140/CTreeCtrl--EnsureVisible.md)   
 [CTreeCtrl::GetParentItem](../vs140/CTreeCtrl--GetParentItem.md)