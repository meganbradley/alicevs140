---
title: "CListCtrl::SetCallbackMask"
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
ms.assetid: aee1fdf9-8919-421d-8c03-cc5af7c38bd1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetCallbackMask
Sets the callback mask for a list view control.  
  
## Syntax  
  
```  
  
      BOOL SetCallbackMask(  
   UINT nMask   
);  
```  
  
#### Parameters  
 `nMask`  
 New value of the callback mask.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#33)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetCallbackMask](../vs140/CListCtrl--GetCallbackMask.md)