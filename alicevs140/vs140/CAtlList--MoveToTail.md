---
title: "CAtlList::MoveToTail"
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
ms.assetid: d2faa024-0abb-4933-bec7-d91636c3740c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::MoveToTail
Call this method to move the specified element to the tail of the list.  
  
## Syntax  
  
```  
  
      void MoveToTail(  
   POSITION pos   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The POSITION value of the element to move.  
  
## Remarks  
 The specified element is moved from its current position to the tail of the list. In debug builds, an assertion failure will occur if `pos` is equal to NULL.  
  
## Example  
 See the example for [CAtlList::MoveToHead](../vs140/CAtlList--MoveToHead.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::MoveToHead](../vs140/CAtlList--MoveToHead.md)   
 [CAtlList::SwapElements](../vs140/CAtlList--SwapElements.md)