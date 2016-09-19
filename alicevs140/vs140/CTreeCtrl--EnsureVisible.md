---
title: "CTreeCtrl::EnsureVisible"
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
ms.assetid: 67e05a30-b716-4e83-9c43-8f89d35aefdd
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::EnsureVisible
Call this function to ensure that a tree view item is visible.  
  
## Syntax  
  
```  
  
      BOOL EnsureVisible(  
   HTREEITEM hItem   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of the tree item being made visible.  
  
## Return Value  
 Returns **TRUE** if the system scrolled the items in the tree-view control to ensure that the specified item is visible. Otherwise, the return value is **FALSE**.  
  
## Remarks  
 If necessary, the function expands the parent item or scrolls the tree view control so that the item is visible.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#6)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetFirstVisibleItem](../vs140/CTreeCtrl--GetFirstVisibleItem.md)   
 [CTreeCtrl::GetVisibleCount](../vs140/CTreeCtrl--GetVisibleCount.md)