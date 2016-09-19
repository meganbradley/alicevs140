---
title: "CTreeCtrl::SelectSetFirstVisible"
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
ms.assetid: 2857f8dc-a77b-483d-b6c2-46187078175b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SelectSetFirstVisible
Call this function to scroll the tree view vertically so that the given item is the first visible item.  
  
## Syntax  
  
```  
  
      BOOL SelectSetFirstVisible(  
   HTREEITEM hItem   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of the tree item to be set as the first visible item.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The function sends a message to the window with the `TVM_SELECTITEM` and `TVGN_FIRSTVISIBLE` message parameters.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#28)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::Select](../vs140/CTreeCtrl--Select.md)   
 [CTreeCtrl::SelectItem](../vs140/CTreeCtrl--SelectItem.md)   
 [CTreeCtrl::SelectDropTarget](../vs140/CTreeCtrl--SelectDropTarget.md)