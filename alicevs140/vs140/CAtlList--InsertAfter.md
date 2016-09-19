---
title: "CAtlList::InsertAfter"
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
ms.assetid: a085421a-1944-43dc-bd6c-36de196cda8c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::InsertAfter
Call this method to insert a new element into the list after the specified position.  
  
## Syntax  
  
```  
  
      POSITION InsertAfter(  
   POSITION pos,  
   INARGTYPE element   
);  
```  
  
#### Parameters  
 `pos`  
 The POSITION value after which the new element will be inserted.  
  
 `element`  
 The element to be inserted.  
  
## Return Value  
 Returns the POSITION value of the new element.  
  
## Remarks  
 In debug builds, an assertion failure will occur if the list isn't valid, if the insert fails, or if an attempt is made to insert the element after the tail.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#23](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#23)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::InsertBefore](../vs140/CAtlList--InsertBefore.md)