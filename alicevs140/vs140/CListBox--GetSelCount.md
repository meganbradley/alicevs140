---
title: "CListBox::GetSelCount"
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
ms.assetid: da9f057c-cb0e-4efa-85c6-99637dd8d40f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetSelCount
Retrieves the total number of selected items in a multiple-selection list box.  
  
## Syntax  
  
```  
  
int GetSelCount( ) const;  
```  
  
## Return Value  
 The count of selected items in a list box. If the list box is a single-selection list box, the return value is **LB_ERR**.  
  
## Example  
 See the example for [CListBox::GetSelItems](../vs140/CListBox--GetSelItems.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::SetSel](../vs140/CListBox--SetSel.md)   
 [LB_GETSELCOUNT](http://msdn.microsoft.com/library/windows/desktop/bb761309)