---
title: "CVSListBox::GetCount"
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
ms.assetid: 6abe5180-750a-461b-ad1d-139aaea241f8
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CVSListBox::GetCount
Retrieves the number of strings in an editable list control.  
  
## Syntax  
  
```  
virtual int GetCount() const;  
```  
  
## Return Value  
 The number of items in the list control.  
  
## Remarks  
 Note that the count is one greater than the index value of the last item because the index is zero-based.  
  
## Requirements  
 **Header:** afxvslistbox.h  
  
## See Also  
 [CVSListBox Class](../vs140/CVSListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)