---
title: "CTreeCtrl::GetItemState"
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
ms.assetid: 904aa149-1658-4d73-82eb-12d9f1d84089
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetItemState
Returns the state of the item specified by `hItem`.  
  
## Syntax  
  
```  
  
      UINT GetItemState(  
   HTREEITEM hItem,  
   UINT nStateMask   
) const;  
```  
  
#### Parameters  
 `hItem`  
 Handle of the item whose state is to be retrieved.  
  
 `nStateMask`  
 Mask indicating one or more states to be retrieved. For more information on possible values for `nStateMask`, see the discussion of the **state** and **stateMask** members of the [TVITEM](http://msdn.microsoft.com/library/windows/desktop/bb773456) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 A **UINT** that holds the bitwise OR of the values specified by nStateMask. For information on possible values, see [CTreeCtrl::GetItem](../vs140/CTreeCtrl--GetItem.md). To find the value for a specific state, perform a bitwise AND operation of the state value and the return value, as shown in the following example.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#18)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Tree Control Item States Overview](../vs140/Tree-Control-Item-States-Overview.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetItem](../vs140/CTreeCtrl--GetItem.md)