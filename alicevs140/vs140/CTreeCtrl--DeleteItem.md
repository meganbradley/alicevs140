---
title: "CTreeCtrl::DeleteItem"
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
ms.assetid: 3835f7bc-1f09-4214-b77e-827506f02599
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::DeleteItem
Call this function to delete an item from the tree view control.  
  
## Syntax  
  
```  
  
      BOOL DeleteItem(  
   HTREEITEM hItem   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of the tree item to be deleted. If *hitem* has the **TVI_ROOT** value, all items are deleted from the tree view control.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#4)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::DeleteAllItems](../vs140/CTreeCtrl--DeleteAllItems.md)   
 [CTreeCtrl::InsertItem](../vs140/CTreeCtrl--InsertItem.md)