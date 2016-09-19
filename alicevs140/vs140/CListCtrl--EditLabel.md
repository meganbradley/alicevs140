---
title: "CListCtrl::EditLabel"
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
ms.assetid: 597a0c1c-a6d0-442e-9d1c-1c10e267e1bf
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::EditLabel
Begins in-place editing of an item's text.  
  
## Syntax  
  
```  
  
      CEdit* EditLabel(  
   int nItem   
);  
```  
  
#### Parameters  
 `nItem`  
 Index of the list view item that is to be edited.  
  
## Return Value  
 If successful, a pointer to the `CEdit` object that is used to edit the item text; otherwise **NULL**.  
  
## Remarks  
 A list view control that has the `LVS_EDITLABELS` window style enables a user to edit item labels in place. The user begins editing by clicking the label of an item that has the focus.  
  
 Use this function to begin in-place editing of the specified list view item's text.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#7)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetEditControl](../vs140/CListCtrl--GetEditControl.md)