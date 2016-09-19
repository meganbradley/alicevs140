---
title: "CTreeCtrl::SetItemText"
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
ms.assetid: f6a3e0e0-c92e-4ce1-a0f5-7838b00a5b64
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetItemText
Sets the text of the item specified by `hItem`.  
  
## Syntax  
  
```  
  
      BOOL SetItemText(  
   HTREEITEM hItem,  
   LPCTSTR lpszItem   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of the item whose text is to be set.  
  
 `lpszItem`  
 Address of a string containing the new text for the item  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#34)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetItemText](../vs140/CTreeCtrl--GetItemText.md)