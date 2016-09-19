---
title: "CAtlList::RemoveTail"
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
ms.assetid: 9de7cbbe-7a8b-45ad-8d56-77550de78357
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::RemoveTail
Call this method to remove the element at the tail of the list.  
  
## Syntax  
  
```  
  
E RemoveTail( );  
  
```  
  
## Return Value  
 Returns the element at the tail of the list.  
  
## Remarks  
 The tail element is deleted from the list, and memory is freed. A copy of the element is returned. In debug builds, an assertion failure will occur if the list is empty.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#29](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#29)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::RemoveTailNoReturn](../vs140/CAtlList--RemoveTailNoReturn.md)   
 [CAtlList::RemoveHead](../vs140/CAtlList--RemoveHead.md)   
 [CAtlList::RemoveHeadNoReturn](../vs140/CAtlList--RemoveHeadNoReturn.md)