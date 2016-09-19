---
title: "CTreeCtrl::ItemHasChildren"
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
ms.assetid: b432c2f4-ddef-479b-8337-606d289ecf37
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::ItemHasChildren
Use this function to determine whether the tree item specified by `hItem` has child items.  
  
## Syntax  
  
```  
  
      BOOL ItemHasChildren(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
## Return Value  
 Nonzero if the tree item specified by `hItem` has child items; 0 if it does not.  
  
## Remarks  
 If so, you can then use [CTreeCtrl::GetChildItem](../vs140/CTreeCtrl--GetChildItem.md) to retrieve those child items.  
  
## Example  
 See the example for [CTreeCtrl::GetSelectedItem](../vs140/CTreeCtrl--GetSelectedItem.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetChildItem](../vs140/CTreeCtrl--GetChildItem.md)