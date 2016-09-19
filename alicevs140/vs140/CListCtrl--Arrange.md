---
title: "CListCtrl::Arrange"
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
ms.assetid: 43235a7a-58d3-4780-8bcd-99b35c60eca0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::Arrange
Repositions items in an icon view so that they align on a grid.  
  
## Syntax  
  
```  
  
      BOOL Arrange(  
   UINT nCode   
);  
```  
  
#### Parameters  
 `nCode`  
 Specifies the alignment style for the items. It can be one of the following values:  
  
-   `LVA_ALIGNLEFT` Aligns items along the left edge of the window.  
  
-   `LVA_ALIGNTOP` Aligns items along the top edge of the window.  
  
-   `LVA_DEFAULT` Aligns items according to the list view's current alignment styles (the default value).  
  
-   `LVA_SNAPTOGRID` Snaps all icons to the nearest grid position.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The `nCode` parameter specifies the alignment style.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#2)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::EnsureVisible](../vs140/CListCtrl--EnsureVisible.md)