---
title: "CTreeCtrl::SetCheck"
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
ms.assetid: 076496cd-aa42-413a-a3c8-e8be0dd393af
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetCheck
Call this member function to set the check state for a tree control item.  
  
## Syntax  
  
```  
  
      BOOL SetCheck(  
   HTREEITEM hItem,  
   BOOL fCheck = TRUE   
);  
```  
  
#### Parameters  
 `hItem`  
 The **HTREEITEM** to receive the check state change.  
  
 `fCheck`  
 Indicates whether the tree control item is to be checked or unchecked. By default, `SetCheck` sets the item to be checked.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 When the tree control item is checked (`fCheck` set to **TRUE**), the item appears with an adjacent checkmark.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#29)]  
  
## Example  
 To use checkboxes, set TVS_CHECKBOXES before populating the tree control.  
  
 [!CODE [NVC_MFC_CTreeCtrl#30](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#30)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetCheck](../vs140/CTreeCtrl--GetCheck.md)