---
title: "CTreeCtrl::GetEditControl"
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
ms.assetid: e4f476f9-4ae8-4518-ad97-1434e9cc7e4f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetEditControl
Call this function to retrieve the handle of the edit control being used to edit a tree view item's text.  
  
## Syntax  
  
```  
  
CEdit* GetEditControl( ) const;  
```  
  
## Return Value  
 A pointer to the edit control used to edit the item text, if successful; otherwise **NULL**.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#10)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::EditLabel](../vs140/CTreeCtrl--EditLabel.md)