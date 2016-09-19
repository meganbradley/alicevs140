---
title: "CListBox::SetCaretIndex"
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
ms.assetid: 1fa7d29c-80d3-4709-b6f3-509513a1a00c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetCaretIndex
Sets the focus rectangle to the item at the specified index in a multiple-selection list box.  
  
## Syntax  
  
```  
  
      int SetCaretIndex(  
   int nIndex,  
   BOOL bScroll = TRUE   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the item to receive the focus rectangle in the list box.  
  
 *bScroll*  
 If this value is 0, the item is scrolled until it is fully visible. If this value is not 0, the item is scrolled until it is at least partially visible.  
  
## Return Value  
 **LB_ERR** if an error occurs.  
  
## Remarks  
 If the item is not visible, it is scrolled into view.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#30](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#30)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::GetCaretIndex](../vs140/CListBox--GetCaretIndex.md)   
 [LB_SETCARETINDEX](http://msdn.microsoft.com/library/windows/desktop/bb761336)