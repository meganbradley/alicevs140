---
title: "CTreeCtrl::GetNextItem"
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
ms.assetid: 0f19ec21-a569-4f9e-b372-eefa821307d5
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetNextItem
Call this function to retrieve the tree view item that has the specified relationship, indicated by the `nCode` parameter, to `hItem`.  
  
## Syntax  
  
```  
  
      HTREEITEM GetNextItem(  
   HTREEITEM hItem,  
   UINT nCode   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of a tree item.  
  
 `nCode`  
 A flag indicating the type of relation to `hItem`. This flag can be one of the following values:  
  
-   `TVGN_CARET` Retrieves the currently selected item.  
  
-   `TVGN_CHILD` Retrieves the first child item of the item specified by the `hItem` parameter.  
  
-   `TVGN_DROPHILITE` Retrieves the item that is the target of a drag-and-drop operation.  
  
-   `TVGN_FIRSTVISIBLE` Retrieves the first visible item.  
  
-   `TVGN_LASTVISIBLE` Retrieves the last expanded item in the tree. This does not retrieve the last item visible in the tree-view window.  
  
-   `TVGN_NEXT` Retrieves the next sibling item.  
  
-   `TVGN_NEXTVISIBLE` Retrieves the next visible item that follows the specified item.  
  
-   `TVGN_PARENT` Retrieves the parent of the specified item.  
  
-   `TVGN_PREVIOUS` Retrieves the previous sibling item.  
  
-   `TVGN_PREVIOUSVISIBLE` Retrieves the first visible item that precedes the specified item.  
  
-   `TVGN_ROOT` Retrieves the first child item of the root item of which the specified item is a part.  
  
## Return Value  
 The handle of the next item if successful; otherwise **NULL**.  
  
## Remarks  
 This function will return **NULL** if the item being retrieved is the root node of the tree. For example, if you use this message with the `TVGN_PARENT` flag on a first-level child of the tree view's root node, the message will return **NULL**.  
  
## Example  
 For an example of using `GetNextItem` in a loop, see [CTreeCtrl::DeleteItem](../vs140/CTreeCtrl--DeleteItem.md).  
  
 [!CODE [NVC_MFC_CTreeCtrl#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#20)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetItem](../vs140/CTreeCtrl--SetItem.md)   
 [CTreeCtrl::GetChildItem](../vs140/CTreeCtrl--GetChildItem.md)   
 [CTreeCtrl::GetItem](../vs140/CTreeCtrl--GetItem.md)   
 [CTreeCtrl::SelectItem](../vs140/CTreeCtrl--SelectItem.md)   
 [CTreeCtrl::GetPrevSiblingItem](../vs140/CTreeCtrl--GetPrevSiblingItem.md)