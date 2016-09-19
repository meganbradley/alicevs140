---
title: "CList::GetCount"
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
ms.assetid: 839f78f3-905f-417b-903c-8f738d0ddf94
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::GetCount
Gets the number of elements in this list.  
  
## Syntax  
  
```  
  
INT_PTR GetCount() const;  
```  
  
## Return Value  
 An integer value containing the element count.  
  
## Remarks  
 Calling this method will generate the same result as the [CList::GetSize](../vs140/CList--GetSize.md) method.  
  
## Example  
 See the example for [CList::RemoveHead](../vs140/CList--RemoveHead.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::IsEmpty](../vs140/CList--IsEmpty.md)   
 [CList::GetSize](../vs140/CList--GetSize.md)