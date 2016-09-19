---
title: "CAtlList::MoveToHead"
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
ms.assetid: 42c70ca8-ea4c-4db3-96ae-0f27f15e6c75
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::MoveToHead
Call this method to move the specified element to the head of the list.  
  
## Syntax  
  
```  
  
      void MoveToHead(  
   POSITION pos   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The POSITION value of the element to move.  
  
## Remarks  
 The specified element is moved from its current position to the head of the list. In debug builds, an assertion failure will occur if `pos` is equal to NULL.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#26](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#26)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::MoveToTail](../vs140/CAtlList--MoveToTail.md)   
 [CAtlList::SwapElements](../vs140/CAtlList--SwapElements.md)