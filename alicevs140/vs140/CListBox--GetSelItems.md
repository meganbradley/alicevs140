---
title: "CListBox::GetSelItems"
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
ms.assetid: 4d7230fb-00c1-408c-9bc8-8dbb063c31c9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetSelItems
Fills a buffer with an array of integers that specifies the item numbers of selected items in a multiple-selection list box.  
  
## Syntax  
  
```  
  
      int GetSelItems(  
   int nMaxItems,  
   LPINT rgIndex   
) const;  
```  
  
#### Parameters  
 `nMaxItems`  
 Specifies the maximum number of selected items whose item numbers are to be placed in the buffer.  
  
 `rgIndex`  
 Specifies a pointer to a buffer large enough for the number of integers specified by `nMaxItems`.  
  
## Return Value  
 The actual number of items placed in the buffer. If the list box is a single-selection list box, the return value is `LB_ERR`.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#20)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_GETSELITEMS](http://msdn.microsoft.com/library/windows/desktop/bb761311)   
 [CListBox::GetSelCount](../vs140/CListBox--GetSelCount.md)