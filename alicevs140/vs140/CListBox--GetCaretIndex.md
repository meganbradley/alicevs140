---
title: "CListBox::GetCaretIndex"
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
ms.assetid: cc5596c2-bbd8-4b16-ac2c-1da68d503b23
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetCaretIndex
Determines the index of the item that has the focus rectangle in a multiple-selection list box.  
  
## Syntax  
  
```  
  
int GetCaretIndex( ) const;  
```  
  
## Return Value  
 The zero-based index of the item that has the focus rectangle in a list box. If the list box is a single-selection list box, the return value is the index of the item that is selected, if any.  
  
## Remarks  
 The item may or may not be selected.  
  
## Example  
 See the example for [CListBox::SetCaretIndex](../vs140/CListBox--SetCaretIndex.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::SetCaretIndex](../vs140/CListBox--SetCaretIndex.md)   
 [LB_GETCARETINDEX](http://msdn.microsoft.com/library/windows/desktop/bb775193)