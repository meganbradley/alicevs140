---
title: "CList::Find"
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
ms.assetid: 1b010598-edc3-425b-a70a-bb6e42c16bcd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::Find
Searches the list sequentially to find the first element matching the specified `searchValue`.  
  
## Syntax  
  
```  
  
      POSITION Find(  
   ARG_TYPE searchValue,  
   POSITION startAfter = NULL  
) const;   
```  
  
#### Parameters  
 `ARG_TYPE`  
 Template parameter specifying the type of the list element (can be a reference).  
  
 `searchValue`  
 The value to be found in the list.  
  
 `startAfter`  
 The start position for the search. If no value is specified, the search begins with the head element.  
  
## Return Value  
 A **POSITION** value that can be used for iteration or object pointer retrieval; **NULL** if the object is not found.  
  
## Example  
 [!CODE [NVC_MFCCollections#39](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#39)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::GetNext](../vs140/CList--GetNext.md)   
 [CList::GetPrev](../vs140/CList--GetPrev.md)