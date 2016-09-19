---
title: "CRBTree::GetNextKey"
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
ms.assetid: b6b6f835-3974-470b-8dcc-266d96878783
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::GetNextKey
Call this method to get the key of an element stored in the tree and advance the position to the next element.  
  
## Syntax  
  
```  
  
      const K& GetNextKey(  
   POSITION& pos   
) const throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
## Return Value  
 Returns a reference to the next key in the tree.  
  
## Remarks  
 Updates the current position counter, `pos`. If there are no more entries in the tree, the position counter is set to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md)   
 [CRBTree::GetNextValue](../vs140/CRBTree--GetNextValue.md)