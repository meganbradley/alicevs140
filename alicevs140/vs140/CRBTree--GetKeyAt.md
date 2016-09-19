---
title: "CRBTree::GetKeyAt"
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
ms.assetid: 1410907d-7775-4c88-b9cc-873a4ef81622
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::GetKeyAt
Call this method to get the key from a given position in the tree.  
  
## Syntax  
  
```  
  
      const K& GetKeyAt(  
   POSITION pos   
) const throw( );  
```  
  
#### Parameters  
 `pos`  
 The position value.  
  
## Return Value  
 Returns the key stored at position `pos` in the tree.  
  
## Remarks  
 If `pos` is not a valid position value, results are unpredictable. In debug builds, an assertion failure will occur if `pos` is equal to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::GetAt](../vs140/CRBTree--GetAt.md)   
 [CRBTree::SetValueAt](../vs140/CRBTree--SetValueAt.md)   
 [CRBTree::GetValueAt](../vs140/CRBTree--GetValueAt.md)