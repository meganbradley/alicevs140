---
title: "CTreeCtrl::GetSelectedItem"
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
ms.assetid: 9897be77-ca12-4420-95db-205297c117e3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetSelectedItem
Call this function to retrieve the currently selected item of the tree view control.  
  
## Syntax  
  
```  
  
HTREEITEM GetSelectedItem( ) const;  
```  
  
## Return Value  
 The handle of the selected item; otherwise **NULL**.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#24](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#24)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::Select](../vs140/CTreeCtrl--Select.md)   
 [CTreeCtrl::SelectDropTarget](../vs140/CTreeCtrl--SelectDropTarget.md)   
 [CTreeCtrl::GetDropHilightItem](../vs140/CTreeCtrl--GetDropHilightItem.md)