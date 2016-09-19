---
title: "CTreeCtrl::GetNextSiblingItem"
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
ms.assetid: 2f31f80e-556e-43c6-9d60-a12a90b031b1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetNextSiblingItem
Call this function to retrieve the next sibling of `hItem`.  
  
## Syntax  
  
```  
  
      HTREEITEM GetNextSiblingItem(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
## Return Value  
 The handle of the next sibling item; otherwise **NULL**.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#21)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetPrevSiblingItem](../vs140/CTreeCtrl--GetPrevSiblingItem.md)   
 [CTreeCtrl::GetChildItem](../vs140/CTreeCtrl--GetChildItem.md)   
 [CTreeCtrl::GetItem](../vs140/CTreeCtrl--GetItem.md)   
 [CTreeCtrl::SelectItem](../vs140/CTreeCtrl--SelectItem.md)   
 [CTreeCtrl::GetParentItem](../vs140/CTreeCtrl--GetParentItem.md)