---
title: "CTypedPtrList::AddTail"
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
ms.assetid: 0289b7cf-ec7b-4b77-8123-5ed04d9d5467
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrList::AddTail
This member function calls `BASE_CLASS`**::AddTail**.  
  
## Syntax  
  
```  
  
      POSITION AddTail(  
   TYPE newElement   
);  
void AddTail(  
   CTypedPtrList<BASE_CLASS,  
   TYPE> *pNewList   
);  
```  
  
#### Parameters  
 *TYPE*  
 Type of the elements stored in the base-class list.  
  
 `newElement`  
 The object pointer to be added to this list. A **NULL** value is allowed.  
  
 `BASE_CLASS`  
 Base class of the typed pointer list class; must be a pointer list class ([CObList](../vs140/CObList-Class.md) or [CPtrList](../vs140/CPtrList-Class.md)).  
  
 `pNewList`  
 A pointer to another [CTypedPtrList](../vs140/CTypedPtrList-Class.md) object. The elements in `pNewList` will be added to this list.  
  
## Return Value  
 The first version returns the **POSITION** value of the newly inserted element.  
  
## Remarks  
 The first version adds a new element after the tail of the list. The second version adds another list of elements after the tail of the list.  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrList Class](../vs140/CTypedPtrList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)