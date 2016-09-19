---
title: "CTreeCtrl::SelectItem"
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
ms.assetid: 7b803d14-cbfd-46c9-9767-9c59a00da6ef
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SelectItem
Call this function to select the given tree view item.  
  
## Syntax  
  
```  
  
      BOOL SelectItem(  
   HTREEITEM hItem   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 If `hItem` is **NULL**, then this function selects no item.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#26)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::Select](../vs140/CTreeCtrl--Select.md)   
 [CTreeCtrl::GetSelectedItem](../vs140/CTreeCtrl--GetSelectedItem.md)   
 [CTreeCtrl::SelectDropTarget](../vs140/CTreeCtrl--SelectDropTarget.md)