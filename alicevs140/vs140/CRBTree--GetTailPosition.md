---
title: "CRBTree::GetTailPosition"
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
ms.assetid: e7685375-bede-4617-bf51-515065c0c3e1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::GetTailPosition
Call this method to get the position value for the element at the tail of the tree.  
  
## Syntax  
  
```  
  
POSITION GetTailPosition( ) const throw( );  
  
```  
  
## Return Value  
 Returns the position value for the element at the tail of the tree.  
  
## Remarks  
 The value returned by `GetTailPosition` can be used with methods such as [CRBTree::GetKeyAt](../vs140/CRBTree--GetKeyAt.md) or [CRBTree::GetPrev](../vs140/CRBTree--GetPrev.md) to traverse the tree and retrieve values.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md)