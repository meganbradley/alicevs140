---
title: "CListCtrl::GetItemData"
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
ms.assetid: d0e1b9b1-dcca-48bb-8b93-75e47ebaf434
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetItemData
Retrieves the 32-bit application-specific value associated with the item specified by `nItem`.  
  
## Syntax  
  
```  
  
      DWORD_PTR GetItemData(  
   int nItem   
) const;  
```  
  
#### Parameters  
 `nItem`  
 Index of the list item whose data is to be retrieved.  
  
## Return Value  
 A 32-bit application-specific value associated with the specified item.  
  
## Remarks  
 This value is the **lParam** member of the [LVITEM](http://msdn.microsoft.com/library/windows/desktop/bb774760) structure, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#21)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetItemData](../vs140/CListCtrl--SetItemData.md)