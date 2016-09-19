---
title: "CList::RemoveTail"
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
ms.assetid: 5a2c6c8e-f785-4ac1-9a68-f293f07d6ef7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::RemoveTail
Removes the element from the tail of the list and returns a pointer to it.  
  
## Syntax  
  
```  
  
TYPE RemoveTail( );  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements in the list.  
  
## Return Value  
 The element that was at the tail of the list.  
  
## Remarks  
 You must ensure that the list is not empty before calling `RemoveTail`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CList--IsEmpty.md) to verify that the list contains elements.  
  
## Example  
 [!CODE [NVC_MFCCollections#54](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#54)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::GetTail](../vs140/CList--GetTail.md)   
 [CList::AddTail](../vs140/CList--AddTail.md)