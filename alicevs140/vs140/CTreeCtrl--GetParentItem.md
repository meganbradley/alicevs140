---
title: "CTreeCtrl::GetParentItem"
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
ms.assetid: a8a42c8a-2da8-4f19-9e73-5f46e0e9f1e9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetParentItem
Call this function to retrieve the parent of `hItem`.  
  
## Syntax  
  
```  
  
      HTREEITEM GetParentItem(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
## Return Value  
 The handle of the parent item; otherwise **NULL**.  
  
## Remarks  
 This function will return **NULL** if the parent of the specified item is the root node of the tree.  
  
## Example  
 See the example for [CTreeCtrl::EnsureVisible](../vs140/CTreeCtrl--EnsureVisible.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetChildItem](../vs140/CTreeCtrl--GetChildItem.md)   
 [CTreeCtrl::GetRootItem](../vs140/CTreeCtrl--GetRootItem.md)   
 [CTreeCtrl::GetItem](../vs140/CTreeCtrl--GetItem.md)   
 [CTreeCtrl::GetPrevSiblingItem](../vs140/CTreeCtrl--GetPrevSiblingItem.md)