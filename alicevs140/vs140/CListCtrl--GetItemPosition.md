---
title: "CListCtrl::GetItemPosition"
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
ms.assetid: 74a95ba4-f295-4503-898f-1993aef2cec9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetItemPosition
Retrieves the position of a list view item.  
  
## Syntax  
  
```  
  
      BOOL GetItemPosition(  
   int nItem,  
   LPPOINT lpPoint   
) const;  
```  
  
#### Parameters  
 `nItem`  
 The index of the item whose position is to be retrieved.  
  
 `lpPoint`  
 Address of a [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805) structure that receives the position of the item's upper-left corner, in view coordinates.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#22)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetItemPosition](../vs140/CListCtrl--SetItemPosition.md)   
 [CListCtrl::GetOrigin](../vs140/CListCtrl--GetOrigin.md)