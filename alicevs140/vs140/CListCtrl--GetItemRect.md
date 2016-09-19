---
title: "CListCtrl::GetItemRect"
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
ms.assetid: fb8f9641-5ceb-49e9-99af-500a8ca981d1
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetItemRect
Retrieves the bounding rectangle for all or part of an item in the current view.  
  
## Syntax  
  
```  
  
      BOOL GetItemRect(  
   int nItem,  
   LPRECT lpRect,  
   UINT nCode   
) const;  
```  
  
#### Parameters  
 `nItem`  
 The index of the item whose position is to be retrieved.  
  
 `lpRect`  
 Address of a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that receives the bounding rectangle.  
  
 `nCode`  
 Portion of the list view item for which to retrieve the bounding rectangle. It can be one of these values:  
  
-   `LVIR_BOUNDS` Returns the bounding rectangle of the entire item, including the icon and label.  
  
-   `LVIR_ICON` Returns the bounding rectangle of the icon or small icon.  
  
-   `LVIR_LABEL` Returns the bounding rectangle of the item text.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#23)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetItemPosition](../vs140/CListCtrl--GetItemPosition.md)   
 [CListCtrl::SetItemPosition](../vs140/CListCtrl--SetItemPosition.md)   
 [CListCtrl::GetOrigin](../vs140/CListCtrl--GetOrigin.md)