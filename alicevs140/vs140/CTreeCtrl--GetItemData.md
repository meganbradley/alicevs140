---
title: "CTreeCtrl::GetItemData"
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
ms.assetid: 1ecc025f-5995-48b1-82ea-cd3aadb58467
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetItemData
Call this function to retrieve the 32-bit application-specific value associated with the specified item.  
  
## Syntax  
  
```  
  
      DWORD_PTR GetItemData(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of the item whose data is to be retrieved.  
  
## Return Value  
 A 32-bit application-specific value associated with the item specified by `hItem`.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#14)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetItemData](../vs140/CTreeCtrl--SetItemData.md)