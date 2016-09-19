---
title: "CList::InsertBefore"
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
ms.assetid: 079eb330-5095-48d2-9f07-45ea338781ad
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::InsertBefore
Adds an element to this list before the element at the specified position.  
  
## Syntax  
  
```  
  
      POSITION InsertBefore(  
   POSITION position,  
   ARG_TYPE newElement   
);  
```  
  
#### Parameters  
 *position*  
 A **POSITION** value returned by a previous `GetNext`, `GetPrev`, or **Find** member function call.  
  
 `ARG_TYPE`  
 Template parameter specifying the type of the list element (can be a reference).  
  
 `newElement`  
 The element to be added to this list.  
  
## Return Value  
 A **POSITION** value that can be used for iteration or list element retrieval.  
  
## Remarks  
 If *position* is **NULL**, the element is inserted at the head of the list.  
  
## Example  
 [!CODE [NVC_MFCCollections#49](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#49)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::Find](../vs140/CList--Find.md)   
 [CList::InsertAfter](../vs140/CList--InsertAfter.md)