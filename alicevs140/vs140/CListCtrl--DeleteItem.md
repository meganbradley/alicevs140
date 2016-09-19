---
title: "CListCtrl::DeleteItem"
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
ms.assetid: 9f1a4325-5fd7-4592-9ee5-33467e36b58e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::DeleteItem
Deletes an item from a list view control.  
  
## Syntax  
  
```  
  
      BOOL DeleteItem(  
   int nItem   
);  
```  
  
#### Parameters  
 `nItem`  
 Specifies the index of the item to be deleted.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#6)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::InsertItem](../vs140/CListCtrl--InsertItem.md)   
 [CListCtrl::DeleteAllItems](../vs140/CListCtrl--DeleteAllItems.md)