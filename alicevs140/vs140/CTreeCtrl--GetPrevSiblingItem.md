---
title: "CTreeCtrl::GetPrevSiblingItem"
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
ms.assetid: 60a15c4b-bc04-4c9b-9865-5e425097b3f9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetPrevSiblingItem
Call this function to retrieve the previous sibling of `hItem`.  
  
## Syntax  
  
```  
  
      HTREEITEM GetPrevSiblingItem(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
## Return Value  
 The handle of the previous sibling; otherwise **NULL**.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#22)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetNextSiblingItem](../vs140/CTreeCtrl--GetNextSiblingItem.md)   
 [CTreeCtrl::GetParentItem](../vs140/CTreeCtrl--GetParentItem.md)   
 [CTreeCtrl::GetChildItem](../vs140/CTreeCtrl--GetChildItem.md)