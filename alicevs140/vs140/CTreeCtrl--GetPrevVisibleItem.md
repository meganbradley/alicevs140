---
title: "CTreeCtrl::GetPrevVisibleItem"
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
ms.assetid: 6ed0fa1b-80f5-4b0b-819c-ecb82c9961d2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetPrevVisibleItem
Call this function to retrieve the previous visible item of `hItem`.  
  
## Syntax  
  
```  
  
      HTREEITEM GetPrevVisibleItem(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
## Return Value  
 The handle of the previous visible item; otherwise **NULL**.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#23)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetNextVisibleItem](../vs140/CTreeCtrl--GetNextVisibleItem.md)   
 [CTreeCtrl::GetFirstVisibleItem](../vs140/CTreeCtrl--GetFirstVisibleItem.md)   
 [CTreeCtrl::EnsureVisible](../vs140/CTreeCtrl--EnsureVisible.md)   
 [CTreeCtrl::GetVisibleCount](../vs140/CTreeCtrl--GetVisibleCount.md)