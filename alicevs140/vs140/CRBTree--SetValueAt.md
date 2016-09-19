---
title: "CRBTree::SetValueAt"
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
ms.assetid: 3ecbdb2f-5a64-4935-b808-64606bba25f1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::SetValueAt
Call this method to change the value stored at a given position in the `CRBTree` object.  
  
## Syntax  
  
```  
  
      void SetValueAt(  
   POSITION pos,  
   VINARGTYPE value   
);  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
 *value*  
 The value to add to the `CRBTree` object.  
  
## Remarks  
 Changes the value element stored at the given position in the `CRBTree` object.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)