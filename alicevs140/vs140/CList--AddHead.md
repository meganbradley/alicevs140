---
title: "CList::AddHead"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 92b288d3-888c-4693-bc54-5ad72735e5f8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::AddHead
Adds a new element or list of elements to the head of this list.  
  
## Syntax  
  
```  
  
      POSITION AddHead(  
   ARG_TYPE newElement   
);  
void AddHead(  
   CList* pNewList   
);  
```  
  
#### Parameters  
 `ARG_TYPE`  
 Template parameter specifying the type of the list element (can be a reference).  
  
 `newElement`  
 The new element.  
  
 `pNewList`  
 A pointer to another `CList` list. The elements in `pNewList` will be added to this list.  
  
## Return Value  
 The first version returns the **POSITION** value of the newly inserted element.  
  
## Remarks  
 The list can be empty before the operation.  
  
## Example  
 [!CODE [NVC_MFCCollections#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#36)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::GetHead](../vs140/CList--GetHead.md)   
 [CList::RemoveHead](../vs140/CList--RemoveHead.md)