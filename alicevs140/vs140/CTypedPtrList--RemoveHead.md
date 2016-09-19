---
title: "CTypedPtrList::RemoveHead"
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
ms.assetid: b998cd6f-5332-44ba-859e-68370c1337b4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrList::RemoveHead
Removes the element from the head of the list and returns it.  
  
## Syntax  
  
```  
  
TYPE RemoveHead( );  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements stored in the list.  
  
## Return Value  
 The pointer previously at the head of the list. This pointer is of the type specified by the template parameter *TYPE*.  
  
## Remarks  
 You must ensure that the list is not empty before calling `RemoveHead`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CObList--IsEmpty.md) to verify that the list contains elements.  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrList Class](../vs140/CTypedPtrList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTypedPtrList::RemoveTail](../vs140/CTypedPtrList--RemoveTail.md)   
 [CObList::IsEmpty](../vs140/CObList--IsEmpty.md)   
 [CObList::GetHead](../vs140/CObList--GetHead.md)   
 [CObList::AddHead](../vs140/CObList--AddHead.md)