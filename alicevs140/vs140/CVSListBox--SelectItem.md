---
title: "CVSListBox::SelectItem"
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
ms.assetid: ffa47ffc-29b0-400e-83e3-0e63fe4326da
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CVSListBox::SelectItem
Selects an editable list control string.  
  
## Syntax  
  
```  
virtual BOOL SelectItem(  
   int iItem   
);  
```  
  
#### Parameters  
 [in] `iItem`  
 The zero-based index of an editable list control item.  
  
## Return Value  
 `TRUE` if this method is successful; otherwise, `FALSE`.  
  
## Remarks  
 This method selects the specified item, and if it is required, scrolls the item into view.  
  
## Requirements  
 **Header:** afxvslistbox.h  
  
## See Also  
 [CVSListBox Class](../vs140/CVSListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)