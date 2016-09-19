---
title: "CListBox::GetItemRect"
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
ms.assetid: d5b13975-84f7-492d-8009-31b07aeb148b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetItemRect
Retrieves the dimensions of the rectangle that bounds a list-box item as it is currently displayed in the list-box window.  
  
## Syntax  
  
```  
  
      int GetItemRect(  
   int nIndex,  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the item.  
  
 `lpRect`  
 Specifies a long pointer to a [RECT](../vs140/RECT-Structure.md) structure that receives the list-box client coordinates of the item.  
  
## Return Value  
 **LB_ERR** if an error occurs.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#18)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_GETITEMRECT](http://msdn.microsoft.com/library/windows/desktop/bb775206)