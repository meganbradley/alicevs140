---
title: "CTypedPtrList::GetPrev"
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
ms.assetid: a2fa87df-9581-4da7-b55b-9ff7fa97492b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrList::GetPrev
Gets the list element identified by `rPosition`, then sets `rPosition` to the **POSITION** value of the previous entry in the list.  
  
## Syntax  
  
```  
  
      TYPE  
      & GetPrev(  
   POSITION& rPosition   
);  
TYPE GetPrev(  
   POSITION& rPosition   
) const;  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements contained in this list.  
  
 `rPosition`  
 A reference to a **POSITION** value returned by a previous `GetPrev` or other member function call.  
  
## Return Value  
 If the list is accessed through a pointer to a **const CTypedPtrList**, then `GetPrev` returns a pointer of the type specified by the template parameter *TYPE*. This allows the function to be used only on the right side of an assignment statement and thus protects the list from modification.  
  
 If the list is accessed directly or through a pointer to a `CTypedPtrList`, then `GetPrev` returns a reference to a pointer of the type specified by the template parameter *TYPE*. This allows the function to be used on either side of an assignment statement and thus allows the list entries to be modified.  
  
## Remarks  
 You can use `GetPrev` in a reverse iteration loop if you establish the initial position with a call to `GetTailPosition` or **Find**.  
  
 You must ensure that your **POSITION** value represents a valid position in the list. If it is invalid, then the Debug version of the Microsoft Foundation Class Library asserts.  
  
 If the retrieved element is the first in the list, then the new value of `rPosition` is set to **NULL**.  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrList Class](../vs140/CTypedPtrList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::Find](../vs140/CObList--Find.md)   
 [CObList::GetTailPosition](../vs140/CObList--GetTailPosition.md)   
 [CObList::GetHeadPosition](../vs140/CObList--GetHeadPosition.md)   
 [CTypedPtrList::GetNext](../vs140/CTypedPtrList--GetNext.md)   
 [CTypedPtrList::GetHead](../vs140/CTypedPtrList--GetHead.md)   
 [CTypedPtrList::GetTail](../vs140/CTypedPtrList--GetTail.md)