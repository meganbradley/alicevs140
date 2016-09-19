---
title: "CRBTree::GetAt"
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
ms.assetid: 86b0c395-93b8-4afb-b8cc-ddd8191e864f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::GetAt
Call this method to get the element at a given position in the tree.  
  
## Syntax  
  
```  
  
      CPair* GetAt(  
   POSITION pos   
) throw( );  
const CPair* GetAt(  
   POSITION pos   
) const throw( );  
void GetAt(  
   POSITION pos,  
   KOUTARGTYPE key,  
   VOUTARGTYPE value   
) const;  
```  
  
#### Parameters  
 `pos`  
 The position value.  
  
 `key`  
 The variable that receives the key.  
  
 *value*  
 The variable that receives the value.  
  
## Return Value  
 The first two forms return a pointer to a [CPair](../vs140/CRBTree--CPair-Class.md). The third form obtains a key and a value for the given position.  
  
## Remarks  
 The position value can be previously determined with a call to a method such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::GetTailPosition](../vs140/CRBTree--GetTailPosition.md).  
  
 In debug builds, an assertion failure will occur if `pos` is equal to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::GetValueAt](../vs140/CRBTree--GetValueAt.md)   
 [CRBTree::GetKeyAt](../vs140/CRBTree--GetKeyAt.md)   
 [CRBTree::SetValueAt](../vs140/CRBTree--SetValueAt.md)