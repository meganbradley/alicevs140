---
title: "CTypedPtrList::GetNext"
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
ms.assetid: 0d2bbeb0-470a-40e6-abba-1857dcdec1f4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrList::GetNext
Gets the list element identified by `rPosition`, then sets `rPosition` to the **POSITION** value of the next entry in the list.  
  
## Syntax  
  
```  
  
      TYPE  
      & GetNext(  
   POSITION& rPosition   
);  
TYPE GetNext(  
   POSITION& rPosition   
) const;  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements contained in this list.  
  
 `rPosition`  
 A reference to a **POSITION** value returned by a previous `GetNext`, `GetHeadPosition`, or other member function call.  
  
## Return Value  
 If the list is accessed through a pointer to a **const CTypedPtrList**, then `GetNext` returns a pointer of the type specified by the template parameter *TYPE*. This allows the function to be used only on the right side of an assignment statement and thus protects the list from modification.  
  
 If the list is accessed directly or through a pointer to a `CTypedPtrList`, then `GetNext` returns a reference to a pointer of the type specified by the template parameter *TYPE*. This allows the function to be used on either side of an assignment statement and thus allows the list entries to be modified.  
  
## Remarks  
 You can use `GetNext` in a forward iteration loop if you establish the initial position with a call to `GetHeadPosition` or [CPtrList::Find](../vs140/CObList--Find.md).  
  
 You must ensure that your **POSITION** value represents a valid position in the list. If it is invalid, then the Debug version of the Microsoft Foundation Class Library asserts.  
  
 If the retrieved element is the last in the list, then the new value of `rPosition` is set to **NULL**.  
  
 It is possible to remove an element during an iteration. See the example for [CObList::RemoveAt](../vs140/CObList--RemoveAt.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrList Class](../vs140/CTypedPtrList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::Find](../vs140/CObList--Find.md)   
 [CObList::GetHeadPosition](../vs140/CObList--GetHeadPosition.md)   
 [CObList::GetTailPosition](../vs140/CObList--GetTailPosition.md)   
 [CTypedPtrList::GetPrev](../vs140/CTypedPtrList--GetPrev.md)   
 [CTypedPtrList::GetHead](../vs140/CTypedPtrList--GetHead.md)   
 [CTypedPtrList::GetTail](../vs140/CTypedPtrList--GetTail.md)