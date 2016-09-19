---
title: "CTabCtrl::DeleteItem"
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
ms.assetid: 5c8319f6-836a-4af6-a339-742dd84740a0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::DeleteItem
Removes the specified item from a tab control.  
  
## Syntax  
  
```  
  
      BOOL DeleteItem(  
  int nItem   
);  
```  
  
#### Parameters  
 `nItem`  
 Zero-based value of the item to delete.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CTabCtrl#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTabCtrl#3)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::DeleteAllItems](../vs140/CTabCtrl--DeleteAllItems.md)