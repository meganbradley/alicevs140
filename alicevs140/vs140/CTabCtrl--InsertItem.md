---
title: "CTabCtrl::InsertItem"
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
ms.assetid: bb483ef9-baed-413f-86c8-31864c522259
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::InsertItem
Inserts a new tab in an existing tab control.  
  
## Syntax  
  
```  
  
      LONG InsertItem(  
  int nItem,  
  TCITEM* pTabCtrlItem   
);  
LONG InsertItem(  
  int nItem,  
  LPCTSTR lpszItem   
);  
LONG InsertItem(  
  int nItem,  
  LPCTSTR lpszItem,  
  int nImage   
);  
LONG InsertItem(  
  UINT nMask,  
  int nItem,  
  LPCTSTR lpszItem,  
  int nImage,  
  LPARAM lParam   
);  
LONG InsertItem(   
   UINT nMask,   
   int nItem,   
   LPCTSTR lpszItem,   
   int nImage,   
   LPARAM lParam,   
   DWORD dwState,   
   DWORD dwStateMask   
);  
```  
  
#### Parameters  
 `nItem`  
 Zero-based index of the new tab.  
  
 `pTabCtrlItem`  
 Pointer to a [TCITEM](http://msdn.microsoft.com/library/windows/desktop/bb760554) structure that specifies the attributes of the tab.  
  
 `lpszItem`  
 Address of a null-terminated string that contains the text of the tab.  
  
 `nImage`  
 The zero-based index of an image to insert from an image list.  
  
 `nMask`  
 Specifies which `TCITEM` structure attributes to set. Can be zero or a combination of the following values:  
  
-   `TCIF_TEXT` The **pszText** member is valid.  
  
-   `TCIF_IMAGE` The `iImage` member is valid.  
  
-   `TCIF_PARAM` The **lParam** member is valid.  
  
-   `TCIF_RTLREADING` The text of **pszText** is displayed using right-to-left reading order on Hebrew or Arabic systems.  
  
-   `TCIF_STATE` The **dwState** member is valid.  
  
 `lParam`  
 Application-defined data associated with the tab.  
  
 `dwState`  
 Specifies values for the item's states. For more information, see [TCITEM](http://msdn.microsoft.com/library/windows/desktop/bb760554) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 *dwStateMask*  
 Specifies which states are to be set. For more information, see [TCITEM](http://msdn.microsoft.com/library/windows/desktop/bb760554) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Zero-based index of the new tab if successful; otherwise – 1.  
  
## Example  
 [!CODE [NVC_MFC_CTabCtrl#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTabCtrl#5)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::GetItem](../vs140/CTabCtrl--GetItem.md)   
 [CTabCtrl::SetItem](../vs140/CTabCtrl--SetItem.md)