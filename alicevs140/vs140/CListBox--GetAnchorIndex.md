---
title: "CListBox::GetAnchorIndex"
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
ms.assetid: ba2331d0-403f-4061-b905-b4b0f4314475
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetAnchorIndex
Retrieves the zero-based index of the current anchor item in the list box.  
  
## Syntax  
  
```  
  
int GetAnchorIndex( ) const;  
```  
  
## Return Value  
 The index of the current anchor item, if successful; otherwise **LB_ERR**.  
  
## Remarks  
 In a multiple-selection list box, the anchor item is the first or last item in a block of contiguous selected items.  
  
## Example  
 See the example for [CListBox::SetAnchorIndex](../vs140/CListBox--SetAnchorIndex.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::SetAnchorIndex](../vs140/CListBox--SetAnchorIndex.md)