---
title: "CListBox::ItemFromPoint"
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
ms.assetid: 2f4be783-9e0e-4601-b491-b6bab78db188
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::ItemFromPoint
Determines the list-box item nearest the point specified in `pt`.  
  
## Syntax  
  
```  
UINT ItemFromPoint(  
   CPoint pt,  
   BOOL& bOutside  
) const;  
```  
  
#### Parameters  
 `pt`  
 Point for which to find the nearest item, specified relative to the upper-left corner of the client area of the list box.  
  
 `bOutside`  
 Reference to a `BOOL` variable which will be set to `TRUE` if `pt` is outside the client area of the nearest list box item, `FALSE` if `pt` is inside the client area of the nearest list box item.  
  
## Return Value  
 The index of the nearest item to the point specified in `pt`.  
  
## Remarks  
 You could use this function to determine which list-box item the mouse cursor moves over.  
  
## Example  
 See the example for [CListBox::SetAnchorIndex](../vs140/CListBox--SetAnchorIndex.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::GetItemRect](../vs140/CListBox--GetItemRect.md)   
 [LB_ITEMFROMPOINT](http://msdn.microsoft.com/library/windows/desktop/bb761323)