---
title: "CAtlList::Find"
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
ms.assetid: 6e3b3cd9-a304-40f0-a887-a9961235fa37
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::Find
Call this method to search the list for the specified element.  
  
## Syntax  
  
```  
  
      POSITION Find(  
   INARGTYPE element,  
   POSITION posStartAfter = NULL   
) const throw( );  
```  
  
#### Parameters  
 `element`  
 The element to be found in the list.  
  
 `posStartAfter`  
 The start position for the search. If no value is specified, the search begins with the head element.  
  
## Return Value  
 Returns the POSITION value of the element if found, otherwise returns NULL.  
  
## Remarks  
 In debug builds, an assertion failure will occur if the list object is not valid, or if the `posStartAfter` value is out of range.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#19](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#19)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::FindIndex](../vs140/CAtlList--FindIndex.md)