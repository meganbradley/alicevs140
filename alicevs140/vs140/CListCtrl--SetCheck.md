---
title: "CListCtrl::SetCheck"
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
ms.assetid: cf7a2785-a6fb-4c46-84c8-3c40fb9be5bd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetCheck
Determines if the state image of a list control item is visible.  
  
## Syntax  
  
```  
  
      BOOL SetCheck(  
   int nItem,  
   BOOL fCheck = TRUE   
);  
```  
  
#### Parameters  
 `nItem`  
 The zero-based index of a list control item.  
  
 `fCheck`  
 Specifies whether the state image of the item should be visible or not. By default, *fCheck* is **TRUE** and the state image is visible. If `fCheck` is **FALSE**, it is not visible.  
  
## Return Value  
 Nonzero if the item is checked, otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#43](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#43)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetCheck](../vs140/CListCtrl--GetCheck.md)