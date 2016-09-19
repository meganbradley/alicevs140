---
title: "CAtlList::GetPrev"
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
ms.assetid: b10a936a-615e-48ac-a1e2-9553db2310e1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::GetPrev
Call this method to return the previous element from the list.  
  
## Syntax  
  
```  
  
      E& GetPrev(  
   POSITION& pos   
) throw( );  
const E& GetPrev(  
   POSITION& pos   
) const throw( );  
```  
  
#### Parameters  
 `pos`  
 A POSITION value, returned by a previous call to `GetPrev`, [CAtlList::GetTailPosition](../vs140/CAtlList--GetTailPosition.md), or other `CAtlList` method.  
  
## Return Value  
 If the list is **const**, `GetPrev` returns a copy of an element of the list. This allows the method to be used only on the right side of an assignment statement and protects the list from modification.  
  
 If the list is not **const**, `GetPrev` returns a reference to an element of the list. This allows the method to be used on either side of an assignment statement and thus allows the list entries to be modified.  
  
## Remarks  
 The POSITION counter, `pos`, is updated to point to the previous element in the list, or NULL if there are no more elements. In debug builds, an assertion failure will occur if `pos` is equal to NULL.  
  
## Example  
 See the example for [CAtlList::GetTailPosition](../vs140/CAtlList--GetTailPosition.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::GetNext](../vs140/CAtlList--GetNext.md)