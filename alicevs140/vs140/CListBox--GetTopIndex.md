---
title: "CListBox::GetTopIndex"
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
ms.assetid: 25c150a4-a559-4a0d-9729-f4b0373c46a9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetTopIndex
Retrieves the zero-based index of the first visible item in a list box.  
  
## Syntax  
  
```  
  
int GetTopIndex( ) const;  
```  
  
## Return Value  
 The zero-based index of the first visible item in a list box if successful, **LB_ERR** otherwise.  
  
## Remarks  
 Initially, item 0 is at the top of the list box, but if the list box is scrolled, another item may be at the top.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#22)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::SetTopIndex](../vs140/CListBox--SetTopIndex.md)   
 [LB_GETTOPINDEX](http://msdn.microsoft.com/library/windows/desktop/bb761317)