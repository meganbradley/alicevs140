---
title: "CAtlList::InsertBefore"
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
ms.assetid: 9353d42f-9d11-476f-8ff5-e0f45b6e054a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::InsertBefore
Call this method to insert a new element into the list before the specified position.  
  
## Syntax  
  
```  
  
      POSITION InsertBefore(  
   POSITION pos,  
   INARGTYPE element   
);  
```  
  
#### Parameters  
 `pos`  
 The new element will be inserted into the list before this POSITION value.  
  
 `element`  
 The element to be inserted.  
  
## Return Value  
 Returns the POSITION value of the new element.  
  
## Remarks  
 In debug builds, an assertion failure will occur if the list isn't valid, if the insert fails, or if an attempt is made to insert the element before the head.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#24](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#24)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::InsertAfter](../vs140/CAtlList--InsertAfter.md)