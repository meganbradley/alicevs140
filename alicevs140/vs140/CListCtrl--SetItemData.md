---
title: "CListCtrl::SetItemData"
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
ms.assetid: 95466ab7-71ad-459f-8faa-92b70c270c2a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetItemData
Sets the 32-bit application-specific value associated with the item specified by `nItem`.  
  
## Syntax  
  
```  
  
      BOOL SetItemData(  
   int nItem,  
   DWORD_PTR dwData   
);  
```  
  
#### Parameters  
 `nItem`  
 Index of the list item whose data is to be set.  
  
 `dwData`  
 A 32-bit value to be associated with the item.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This value is the **lParam** member of the [LVITEM](http://msdn.microsoft.com/library/windows/desktop/bb774760) structure, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#37](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#37)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetItemData](../vs140/CListCtrl--GetItemData.md)