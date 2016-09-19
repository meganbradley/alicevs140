---
title: "CListCtrl::DeleteColumn"
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
ms.assetid: c9ea2506-36f1-494b-8f74-f5b2e8ecc0f4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::DeleteColumn
Deletes a column from the list view control.  
  
## Syntax  
  
```  
  
      BOOL DeleteColumn(  
   int nCol   
);  
```  
  
#### Parameters  
 `nCol`  
 Index of the column to be deleted.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#5)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::InsertColumn](../vs140/CListCtrl--InsertColumn.md)   
 [CListCtrl::DeleteAllItems](../vs140/CListCtrl--DeleteAllItems.md)