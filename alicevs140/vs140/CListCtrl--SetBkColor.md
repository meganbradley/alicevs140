---
title: "CListCtrl::SetBkColor"
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
ms.assetid: 0e5204fd-6410-4944-8c25-bead7b758eb9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetBkColor
Sets the background color of the list view control.  
  
## Syntax  
  
```  
  
      BOOL SetBkColor(  
   COLORREF cr   
);  
```  
  
#### Parameters  
 `cr`  
 Background color to set, or the `CLR_NONE` value for no background color. List view controls with background colors redraw themselves significantly faster than those without background colors. For information, see [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#32](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#32)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetBkColor](../vs140/CListCtrl--GetBkColor.md)