---
title: "CTypedPtrList::RemoveTail"
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
ms.assetid: 4bb352cf-437f-4e8b-96f2-62b49a659817
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrList::RemoveTail
Removes the element from the tail of the list and returns it.  
  
## Syntax  
  
```  
  
TYPE RemoveTail( );  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements stored in the list.  
  
## Return Value  
 The pointer previously at the tail of the list. This pointer is of the type specified by the template parameter *TYPE*.  
  
## Remarks  
 You must ensure that the list is not empty before calling `RemoveTail`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CObList--IsEmpty.md) to verify that the list contains elements.  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrList Class](../vs140/CTypedPtrList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTypedPtrList::RemoveHead](../vs140/CTypedPtrList--RemoveHead.md)   
 [CObList::IsEmpty](../vs140/CObList--IsEmpty.md)   
 [CObList::GetTail](../vs140/CObList--GetTail.md)   
 [CObList::AddTail](../vs140/CObList--AddTail.md)