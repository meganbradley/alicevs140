---
title: "CTreeCtrl::GetChildItem"
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
ms.assetid: fde6e18f-e954-4892-b472-474015e4fff9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetChildItem
Call this function to retrieve the tree view item that is the child of the item specified by `hItem`.  
  
## Syntax  
  
```  
  
      HTREEITEM GetChildItem(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
## Return Value  
 The handle of the child item if successful; otherwise **NULL**.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#7)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetItem](../vs140/CTreeCtrl--GetItem.md)   
 [CTreeCtrl::GetParentItem](../vs140/CTreeCtrl--GetParentItem.md)   
 [CTreeCtrl::SortChildren](../vs140/CTreeCtrl--SortChildren.md)