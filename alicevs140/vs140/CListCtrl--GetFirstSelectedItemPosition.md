---
title: "CListCtrl::GetFirstSelectedItemPosition"
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
ms.assetid: 6d6a849e-c08b-4e5b-ad17-07162ffdbb80
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetFirstSelectedItemPosition
Gets the position of the first selected item in the list view control.  
  
## Syntax  
  
```  
  
POSITION GetFirstSelectedItemPosition( ) const;  
  
```  
  
## Return Value  
 A **POSITION** value that can be used for iteration or object pointer retrieval; **NULL** if no items are selected.  
  
## Example  
 The following code sample demonstrates the usage of this function.  
  
 [!CODE [NVC_MFC_CListCtrl#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#15)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList Class](../vs140/CImageList-Class.md)   
 [CListCtrl::GetNextSelectedItem](../vs140/CListCtrl--GetNextSelectedItem.md)