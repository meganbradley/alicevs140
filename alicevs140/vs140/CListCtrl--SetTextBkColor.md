---
title: "CListCtrl::SetTextBkColor"
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
ms.assetid: 81712496-3b43-435a-8b4b-5edeb675cfca
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetTextBkColor
Sets the background color of text in a list view control.  
  
## Syntax  
  
```  
  
      BOOL SetTextBkColor(  
   COLORREF cr   
);  
```  
  
#### Parameters  
 `cr`  
 A **COLORREF** specifying the new text background color. For information, see [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#24](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#24)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetTextBkColor](../vs140/CListCtrl--GetTextBkColor.md)