---
title: "CRBTree::GetHeadPosition"
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
ms.assetid: 2b7a2efe-e977-4cb0-976a-095d4d1f6a30
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::GetHeadPosition
Call this method to get the position value for the element at the head of the tree.  
  
## Syntax  
  
```  
  
POSITION GetHeadPosition( ) const throw( );  
  
```  
  
## Return Value  
 Returns the position value for the element at the head of the tree.  
  
## Remarks  
 The value returned by `GetHeadPosition` can be used with methods such as [CRBTree::GetKeyAt](../vs140/CRBTree--GetKeyAt.md) or [CRBTree::GetNext](../vs140/CRBTree--GetNext.md) to traverse the tree and retrieve values.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::GetTailPosition](../vs140/CRBTree--GetTailPosition.md)