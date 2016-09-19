---
title: "CTreeCtrl::SortChildren"
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
ms.assetid: 1f724529-8853-4691-988a-407222af158c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SortChildren
Call this function to alphabetically sort the child items of the given parent item in a tree view control.  
  
## Syntax  
  
```  
  
      BOOL SortChildren(  
   HTREEITEM hItem   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of the parent item whose child items are to be sorted. If `hItem` is **NULL**, sorting will proceed from the root of the tree.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 `SortChildren` will not recurse through the tree; only the immediate children of `hItem` will be sorted.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#37](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#37)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SortChildrenCB](../vs140/CTreeCtrl--SortChildrenCB.md)