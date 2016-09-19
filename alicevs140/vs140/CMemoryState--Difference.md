---
title: "CMemoryState::Difference"
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
ms.assetid: aba69e2f-71dd-4255-99b5-3da2e56a0c9c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMemoryState::Difference
Compares two `CMemoryState` objects, then stores the difference into this `CMemoryState` object.  
  
## Syntax  
  
```  
  
      BOOL Difference(  
  const CMemoryState& oldState,  
  const CMemoryState& newState   
);  
```  
  
#### Parameters  
 *oldState*  
 The initial memory state as defined by a `CMemoryState` checkpoint.  
  
 *newState*  
 The new memory state as defined by a `CMemoryState` checkpoint.  
  
## Return Value  
 Nonzero if the two memory states are different; otherwise 0.  
  
## Remarks  
 [Checkpoint](../vs140/CMemoryState--Checkpoint.md) must have been called for each of the two memory-state parameters.  
  
## Example  
 See the example for the [CMemoryState](../vs140/CMemoryState--CMemoryState.md) constructor.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CMemoryState Structure](../vs140/CMemoryState-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)