---
title: "CListCtrl::GetHotItem"
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
ms.assetid: be3fa7fe-cc0a-43a8-8707-32da187855ac
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetHotItem
Retrieves the list view item currently under the cursor.  
  
## Syntax  
  
```  
  
int GetHotItem( );  
  
```  
  
## Return Value  
 The index of the current hot item of the list view control.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_GetHotItem](http://msdn.microsoft.com/library/windows/desktop/bb761294), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The hot item is defined as the currently selected item when hot tracking (and hover selection) is enabled.  
  
 If hot tracking is enabled, when a user pauses over a list view item, the item label is automatically highlighted without the use of a mouse button.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#18)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetHotCursor](../vs140/CListCtrl--GetHotCursor.md)