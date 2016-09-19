---
title: "CListBox::SetAnchorIndex"
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
ms.assetid: 76ef39d7-b5a6-4d9e-8951-54df4ab33200
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetAnchorIndex
Sets the anchor in a multiple-selection list box to begin an extended selection.  
  
## Syntax  
  
```  
  
      void SetAnchorIndex(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the list-box item that will be the anchor.  
  
## Remarks  
 In a multiple-selection list box, the anchor item is the first or last item in a block of contiguous selected items.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#29)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::GetAnchorIndex](../vs140/CListBox--GetAnchorIndex.md)