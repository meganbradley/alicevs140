---
title: "CListCtrl::GetHotCursor"
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
ms.assetid: 4d50e262-6377-44a1-8a93-bfa70a551490
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetHotCursor
Retrieves the cursor used when hot tracking is enabled for a list view control.  
  
## Syntax  
  
```  
  
HCURSOR GetHotCursor( );  
  
```  
  
## Return Value  
 The handle to the current hot cursor resource being used by the list view control.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_GetHotCursor](http://msdn.microsoft.com/library/windows/desktop/bb761292), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The hot cursor, only visible when hover selection is enabled, appears when the cursor passes over any list view item. Hover selection is enabled by setting the **LVS_EX_TRACKSELECT** extended style.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#17)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetHotCursor](../vs140/CListCtrl--SetHotCursor.md)   
 [CListCtrl::GetHotItem](../vs140/CListCtrl--GetHotItem.md)