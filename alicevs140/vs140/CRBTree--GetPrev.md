---
title: "CRBTree::GetPrev"
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
ms.assetid: aa08344c-3a8d-40dd-aca5-30baedc23e83
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::GetPrev
Call this method to obtain a pointer to an element stored in the `CRBTree` object, and then update the position to the previous element.  
  
## Syntax  
  
```  
  
      const CPair* GetPrev(  
   POSITION& pos   
) const throw( );  
CPair* GetPrev(  
   POSITION& pos   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
## Return Value  
 Returns a pointer to the previous [CPair](../vs140/CRBTree--CPair-Class.md) value stored in the tree.  
  
## Remarks  
 Updates the current position counter, `pos`. If there are no more entries in the tree, the position counter is set to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::GetNext](../vs140/CRBTree--GetNext.md)