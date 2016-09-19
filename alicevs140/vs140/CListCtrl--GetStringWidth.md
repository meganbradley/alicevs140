---
title: "CListCtrl::GetStringWidth"
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
ms.assetid: 0dc82110-6552-4020-b192-ce35642c9082
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetStringWidth
Determines the minimum column width necessary to display all of a given string.  
  
## Syntax  
  
```  
  
      int GetStringWidth(  
   LPCTSTR lpsz   
) const;  
```  
  
#### Parameters  
 `lpsz`  
 Address of a null-terminated string whose width is to be determined.  
  
## Return Value  
 The width, in pixels, of the string pointed to by `lpsz`.  
  
## Remarks  
 The returned width takes into account the control's current font and column margins, but not the width of a small icon.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#28)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetColumnWidth](../vs140/CListCtrl--GetColumnWidth.md)