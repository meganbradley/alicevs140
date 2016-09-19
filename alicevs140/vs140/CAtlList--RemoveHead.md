---
title: "CAtlList::RemoveHead"
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
ms.assetid: cbb91bda-f376-44f8-b99a-99ce91d874f0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::RemoveHead
Call this method to remove the element at the head of the list.  
  
## Syntax  
  
```  
  
E RemoveHead( );  
  
```  
  
## Return Value  
 Returns the element at the head of the list.  
  
## Remarks  
 The head element is deleted from the list, and memory is freed. A copy of the element is returned. In debug builds, an assertion failure will occur if the list is empty.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#28](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#28)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::RemoveHeadNoReturn](../vs140/CAtlList--RemoveHeadNoReturn.md)