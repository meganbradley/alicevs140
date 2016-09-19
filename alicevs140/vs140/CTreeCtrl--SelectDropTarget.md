---
title: "CTreeCtrl::SelectDropTarget"
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
ms.assetid: facb4229-2650-4e19-abab-203baa6af09c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SelectDropTarget
Call this function to redraw the item in the style used to indicate the target of a drag-and-drop operation.  
  
## Syntax  
  
```  
  
      BOOL SelectDropTarget(  
   HTREEITEM hItem   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#9)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SelectItem](../vs140/CTreeCtrl--SelectItem.md)   
 [CTreeCtrl::GetDropHilightItem](../vs140/CTreeCtrl--GetDropHilightItem.md)   
 [CTreeCtrl::CreateDragImage](../vs140/CTreeCtrl--CreateDragImage.md)