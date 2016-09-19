---
title: "CTreeCtrl::GetDropHilightItem"
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
ms.assetid: b7de948d-6a46-478e-89f5-3e4bc68b481f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetDropHilightItem
Call this function to retrieve the item that is the target of a drag-and-drop operation.  
  
## Syntax  
  
```  
  
HTREEITEM GetDropHilightItem( ) const;  
```  
  
## Return Value  
 The handle of the item dropped if successful; otherwise **NULL**.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#9)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SelectDropTarget](../vs140/CTreeCtrl--SelectDropTarget.md)