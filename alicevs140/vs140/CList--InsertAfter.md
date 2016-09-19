---
title: "CList::InsertAfter"
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
ms.assetid: f8484253-20ca-45ec-9c70-10390f29e218
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::InsertAfter
Adds an element to this list after the element at the specified position.  
  
## Syntax  
  
```  
  
      POSITION InsertAfter(  
   POSITION position,  
   ARG_TYPE newElement   
);  
```  
  
#### Parameters  
 *position*  
 A **POSITION** value returned by a previous `GetNext`, `GetPrev`, or **Find** member function call.  
  
 `ARG_TYPE`  
 Template parameter specifying the type of the list element.  
  
 `newElement`  
 The element to be added to this list.  
  
## Return Value  
 A **POSITION** value that can be used for iteration or list element retrieval.  
  
## Example  
 [!CODE [NVC_MFCCollections#48](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#48)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::Find](../vs140/CList--Find.md)   
 [CList::InsertBefore](../vs140/CList--InsertBefore.md)