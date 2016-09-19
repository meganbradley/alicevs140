---
title: "CListCtrl::GetEditControl"
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
ms.assetid: 586a00c6-c64c-4d48-b488-1362e8c6922e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetEditControl
Retrieves the handle of the edit control used to edit a list view item's text.  
  
## Syntax  
  
```  
  
CEdit* GetEditControl( ) const;  
```  
  
## Return Value  
 If successful, a pointer to the [CEdit](../vs140/CEdit-Class.md) object that is used to edit the item text; otherwise **NULL**.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#14)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::EditLabel](../vs140/CListCtrl--EditLabel.md)