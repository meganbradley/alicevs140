---
title: "CListCtrl::SetItemCount"
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
ms.assetid: 90ef08b1-a7c8-44ae-8b13-e3955ddeac01
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetItemCount
Prepares a list view control for adding a large number of items.  
  
## Syntax  
  
```  
  
      void SetItemCount(  
   int nItems   
);  
```  
  
#### Parameters  
 `nItems`  
 Number of items that the control will ultimately contain.  
  
## Remarks  
 To set the item count for a virtual list view control, see [CListCtrl::SetItemCountEx](../vs140/CListCtrl--SetItemCountEx.md).  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetItemCount](http://msdn.microsoft.com/library/windows/desktop/bb775093), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#35](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#35)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetItemCount](../vs140/CListCtrl--GetItemCount.md)   
 [CListCtrl::GetSelectedCount](../vs140/CListCtrl--GetSelectedCount.md)