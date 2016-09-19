---
title: "CListCtrl::GetNextSelectedItem"
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
ms.assetid: 26c65d3a-3253-4e39-a03e-4be037804338
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetNextSelectedItem
Gets the index of the list item identified by `pos`, then sets *pos* to the **POSITION** value.  
  
## Syntax  
  
```  
  
      int GetNextSelectedItem(  
   POSITION& pos   
) const;  
```  
  
#### Parameters  
 `pos`  
 A reference to a **POSITION** value returned by a previous call to `GetNextSelectedItem` or `GetFirstSelectedItemPosition`. The value is updated to the next position by this call.  
  
## Return Value  
 The index of the list item identified by `pos`.  
  
## Remarks  
 You can use `GetNextSelectedItem` in a forward iteration loop if you establish the initial position with a call to `GetFirstSelectedItemPosition`.  
  
 You must ensure that your **POSITION** value is valid. If it is invalid, then the Debug version of the Microsoft Foundation Class Library asserts.  
  
## Example  
 The following code sample demonstrates the usage of this function.  
  
 [!CODE [NVC_MFC_CListCtrl#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#15)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList Class](../vs140/CImageList-Class.md)   
 [CListCtrl::GetFirstSelectedItemPosition](../vs140/CListCtrl--GetFirstSelectedItemPosition.md)