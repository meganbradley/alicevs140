---
title: "CAtlList::GetTailPosition"
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
ms.assetid: b8d91f5e-c4a1-43c0-855f-c6d5aa3be8dd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::GetTailPosition
Call this method to obtain the position of the tail of the list.  
  
## Syntax  
  
```  
  
POSITION GetTailPosition( ) const throw( );  
  
```  
  
## Return Value  
 Returns the POSITION value corresponding to the element at the tail of the list.  
  
## Remarks  
 If the list is empty, the value returned is NULL.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#22](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#22)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::GetTail](../vs140/CAtlList--GetTail.md)   
 [CAtlList::GetHeadPosition](../vs140/CAtlList--GetHeadPosition.md)