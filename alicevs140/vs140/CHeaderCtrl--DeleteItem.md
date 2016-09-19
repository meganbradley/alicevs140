---
title: "CHeaderCtrl::DeleteItem"
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
ms.assetid: 750ce05f-4919-48ea-b734-823efc219ea8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::DeleteItem
Deletes an item from a header control.  
  
## Syntax  
  
```  
  
      BOOL DeleteItem(  
   int nPos   
);  
```  
  
#### Parameters  
 `nPos`  
 Specifies the zero-based index of the item to delete.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#5)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::InsertItem](../vs140/CHeaderCtrl--InsertItem.md)