---
title: "CRBTree::GetNext"
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
ms.assetid: f2bb378d-f06c-4ad6-98c3-92c2f040c1a2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::GetNext
Call this method to obtain a pointer to an element stored in the `CRBTree` object, and advance the position to the next element.  
  
## Syntax  
  
```  
  
      const CPair* GetNext(  
   POSITION& pos   
) const throw( );  
CPair* GetNext(  
   POSITION& pos   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
## Return Value  
 Returns a pointer to the next [CPair](../vs140/CRBTree--CPair-Class.md) value in the tree.  
  
## Remarks  
 The `pos` position counter is updated after each call. If the retrieved element is the last in the tree, `pos` is set to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::GetPrev](../vs140/CRBTree--GetPrev.md)