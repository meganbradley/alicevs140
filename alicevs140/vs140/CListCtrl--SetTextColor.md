---
title: "CListCtrl::SetTextColor"
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
ms.assetid: d33fc4d5-ae56-4c09-b6f9-e514749d7b82
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetTextColor
Sets the text color of a list view control.  
  
## Syntax  
  
```  
  
      BOOL SetTextColor(  
   COLORREF cr   
);  
```  
  
#### Parameters  
 `cr`  
 A **COLORREF** specifying the new text color. For information, see [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#38](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#38)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetTextBkColor](../vs140/CListCtrl--SetTextBkColor.md)