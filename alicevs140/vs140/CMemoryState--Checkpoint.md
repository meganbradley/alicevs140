---
title: "CMemoryState::Checkpoint"
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
ms.assetid: b2d80fea-3d21-457e-816d-b035909bf21a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMemoryState::Checkpoint
Takes a snapshot summary of memory and stores it in this `CMemoryState` object.  
  
## Syntax  
  
```  
  
void Checkpoint( );  
```  
  
## Remarks  
 The `CMemoryState` member functions [Difference](../vs140/CMemoryState--Difference.md) and [DumpAllObjectsSince](../vs140/CMemoryState--DumpAllObjectsSince.md) use this snapshot data.  
  
## Example  
 See the example for the [CMemoryState](../vs140/CMemoryState--CMemoryState.md) constructor.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CMemoryState Structure](../vs140/CMemoryState-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)