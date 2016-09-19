---
title: "CTreeCtrl::GetItemRect"
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
ms.assetid: cbd63555-0586-43ce-b8e5-21b511f4c2bd
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetItemRect
Call this function to retrieve the bounding rectangle for `hItem` and determine whether it is visible or not.  
  
## Syntax  
  
```  
  
      BOOL GetItemRect(  
   HTREEITEM hItem,  
   LPRECT lpRect,  
   BOOL bTextOnly   
) const;  
```  
  
#### Parameters  
 `hItem`  
 The handle of a tree view control item.  
  
 `lpRect`  
 Pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that receives the bounding rectangle. The coordinates are relative to the upper-left corner of the tree view control.  
  
 *bTextOnly*  
 If this parameter is nonzero, the bounding rectangle includes only the text of the item. Otherwise it includes the entire line that the item occupies in the tree view control.  
  
## Return Value  
 Nonzero if the item is visible, with the bounding rectangle contained in `lpRect`. Otherwise, 0 with `lpRect` uninitialized.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#17)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetVisibleCount](../vs140/CTreeCtrl--GetVisibleCount.md)   
 [CTreeCtrl::GetNextVisibleItem](../vs140/CTreeCtrl--GetNextVisibleItem.md)   
 [CTreeCtrl::GetPrevVisibleItem](../vs140/CTreeCtrl--GetPrevVisibleItem.md)   
 [CTreeCtrl::EnsureVisible](../vs140/CTreeCtrl--EnsureVisible.md)