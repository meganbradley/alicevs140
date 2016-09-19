---
title: "CAtlList::GetHeadPosition"
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
ms.assetid: a60cd4b1-6e77-4315-a833-689d2a477223
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::GetHeadPosition
Call this method to obtain the position of the head of the list.  
  
## Syntax  
  
```  
  
POSITION GetHeadPosition( ) const throw( );  
  
```  
  
## Return Value  
 Returns the POSITION value corresponding to the element at the head of the list.  
  
## Remarks  
 If the list is empty, the value returned is NULL.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#21](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#21)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::GetHead](../vs140/CAtlList--GetHead.md)   
 [CAtlList::GetTailPosition](../vs140/CAtlList--GetTailPosition.md)