---
title: "CRBTree::GetValueAt"
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
ms.assetid: 07f6f005-59f2-4467-b571-4b71b12e55e4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::GetValueAt
Call this method to retrieve the value stored at a given position in the `CRBTree` object.  
  
## Syntax  
  
```  
  
      const V& GetValueAt(  
   POSITION pos   
) const throw( );  
V& GetValueAt(  
   POSITION pos   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
## Return Value  
 Returns a reference to the value stored at the given position in the `CRBTree` object.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::GetAt](../vs140/CRBTree--GetAt.md)   
 [CRBTree::GetKeyAt](../vs140/CRBTree--GetKeyAt.md)