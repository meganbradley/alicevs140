---
title: "CListCtrl::EnsureVisible"
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
ms.assetid: d4bd6522-4ca8-4a3e-a2d1-3237bd1b5642
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::EnsureVisible
Ensures that a list view item is at least partially visible.  
  
## Syntax  
  
```  
  
      BOOL EnsureVisible(  
   int nItem,  
   BOOL bPartialOK   
);  
```  
  
#### Parameters  
 `nItem`  
 Index of the list view item that is to be visible.  
  
 `bPartialOK`  
 Specifies whether partial visibility is acceptable.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The list view control is scrolled if necessary. If the `bPartialOK` parameter is nonzero, no scrolling occurs if the item is partially visible.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#8)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::Scroll](../vs140/CListCtrl--Scroll.md)