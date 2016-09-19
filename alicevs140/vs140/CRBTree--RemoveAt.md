---
title: "CRBTree::RemoveAt"
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
ms.assetid: aad8105b-4b82-494a-8375-ddfef1ebd592
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::RemoveAt
Call this method to remove the element at the given position in the **CRBTree** object.  
  
## Syntax  
  
```  
  
      void RemoveAt(  
   POSITION pos   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
## Remarks  
 Removes the key/value pair stored at the specified position. The memory used to store the element is freed. The POSITION referenced by `pos` becomes invalid, and while the POSITION of any other elements in the tree remains valid, they do not necessarily retain the same order.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::RemoveAll](../vs140/CRBTree--RemoveAll.md)