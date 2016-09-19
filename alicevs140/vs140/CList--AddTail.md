---
title: "CList::AddTail"
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
ms.assetid: ca970fbf-5bf6-4273-ab0e-fecbc7123e41
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::AddTail
Adds a new element or list of elements to the tail of this list.  
  
## Syntax  
  
```  
  
      POSITION AddTail(  
   ARG_TYPE newElement   
);  
void AddTail(  
   CList* pNewList   
);  
```  
  
#### Parameters  
 `ARG_TYPE`  
 Template parameter specifying the type of the list element (can be a reference).  
  
 `newElement`  
 The element to be added to this list.  
  
 `pNewList`  
 A pointer to another `CList` list. The elements in `pNewList` will be added to this list.  
  
## Return Value  
 The first version returns the **POSITION** value of the newly inserted element.  
  
## Remarks  
 The list can be empty before the operation.  
  
## Example  
 [!CODE [NVC_MFCCollections#37](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#37)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::GetTail](../vs140/CObList--GetTail.md)   
 [CObList::RemoveTail](../vs140/CObList--RemoveTail.md)