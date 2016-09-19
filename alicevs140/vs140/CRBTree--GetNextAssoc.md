---
title: "CRBTree::GetNextAssoc"
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
ms.assetid: 85ca5023-da96-41f4-84aa-e0bfe909682d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::GetNextAssoc
Call this method to get the key and value of an element stored in the map and advance the position to the next element.  
  
## Syntax  
  
```  
  
      void GetNextAssoc(  
   POSITION& pos,  
   KOUTARGTYPE key,  
   VOUTARGTYPE value   
) const;  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
 `key`  
 Template parameter specifying the type of the tree's key.  
  
 *value*  
 Template parameter specifying the type of the tree's value.  
  
## Remarks  
 The `pos` position counter is updated after each call. If the retrieved element is the last in the tree, `pos` is set to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CRBTree::GetPrev](../vs140/CRBTree--GetPrev.md)   
 [CRBTree::GetNext](../vs140/CRBTree--GetNext.md)   
 [CRBTree::GetAt](../vs140/CRBTree--GetAt.md)