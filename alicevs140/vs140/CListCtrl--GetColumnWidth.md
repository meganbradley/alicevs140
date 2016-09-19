---
title: "CListCtrl::GetColumnWidth"
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
ms.assetid: f645a0ff-165c-4d79-8cdc-7bf6cc2a9313
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetColumnWidth
Retrieves the width of a column in report view or list view.  
  
## Syntax  
  
```  
  
      int GetColumnWidth(  
   int nCol   
) const;  
```  
  
#### Parameters  
 `nCol`  
 Specifies the index of the column whose width is to be retrieved.  
  
## Return Value  
 The width, in pixels, of the column specified by `nCol`.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#13)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetColumnWidth](../vs140/CListCtrl--SetColumnWidth.md)   
 [CListCtrl::GetColumn](../vs140/CListCtrl--GetColumn.md)