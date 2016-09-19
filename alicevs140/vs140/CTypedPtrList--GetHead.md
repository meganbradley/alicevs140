---
title: "CTypedPtrList::GetHead"
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
ms.assetid: 057399a3-183b-4e09-a3aa-015a3f7d05b0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrList::GetHead
Gets the pointer that represents the head element of this list.  
  
## Syntax  
  
```  
  
      TYPE  
      & GetHead( );  
TYPE GetHead( ) const;  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements stored in the list.  
  
## Return Value  
 If the list is accessed through a pointer to a **const CTypedPtrList**, then `GetHead` returns a pointer of the type specified by the template parameter *TYPE*. This allows the function to be used only on the right side of an assignment statement and thus protects the list from modification.  
  
 If the list is accessed directly or through a pointer to a `CTypedPtrList`, then `GetHead` returns a reference to a pointer of the type specified by the template parameter *TYPE*. This allows the function to be used on either side of an assignment statement and thus allows the list entries to be modified.  
  
## Remarks  
 You must ensure that the list is not empty before calling `GetHead`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CObList--IsEmpty.md) to verify that the list contains elements.  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrList Class](../vs140/CTypedPtrList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::IsEmpty](../vs140/CObList--IsEmpty.md)   
 [CTypedPtrList::GetTail](../vs140/CTypedPtrList--GetTail.md)   
 [CTypedPtrList::GetNext](../vs140/CTypedPtrList--GetNext.md)   
 [CTypedPtrList::GetPrev](../vs140/CTypedPtrList--GetPrev.md)