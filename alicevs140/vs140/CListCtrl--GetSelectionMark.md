---
title: "CListCtrl::GetSelectionMark"
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
ms.assetid: d3825f05-e4e6-4060-9acf-ba722542df97
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetSelectionMark
Retrieves the selection mark of a list view control.  
  
## Syntax  
  
```  
  
int GetSelectionMark( );  
  
```  
  
## Return Value  
 The zero-based selection mark, or -1 if there is no selection mark.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_GetSelectionMark](http://msdn.microsoft.com/library/windows/desktop/bb774998), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#27)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetSelectionMark](../vs140/CListCtrl--SetSelectionMark.md)