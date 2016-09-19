---
title: "CAtlList::GetAt"
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
ms.assetid: 71c6470d-696f-4214-8120-feee12ea117d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::GetAt
Call this method to return the element at a specified position in the list.  
  
## Syntax  
  
```  
  
      E& GetAt(  
   POSITION pos   
) throw( );  
const E& GetAt(  
   POSITION pos   
) const throw( );  
```  
  
#### Parameters  
 `pos`  
 The POSITION value specifying a particular element.  
  
## Return Value  
 A reference to, or copy of, the element.  
  
## Remarks  
 If the list is **const**, `GetAt` returns a copy of the element. This allows the method to be used only on the right side of an assignment statement and protects the list from modification.  
  
 If the list is not **const**, `GetAt` returns a reference to the element. This allows the method to be used on either side of an assignment statement and thus allows the list entries to be modified.  
  
 In debug builds, an assertion failure will occur if `pos` is equal to NULL.  
  
## Example  
 See the example for [CAtlList::FindIndex](../vs140/CAtlList--FindIndex.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::FindIndex](../vs140/CAtlList--FindIndex.md)