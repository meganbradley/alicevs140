---
title: "CMemoryState::DumpAllObjectsSince"
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
ms.assetid: a7f89034-bca4-4786-88d5-1571a5425ab2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMemoryState::DumpAllObjectsSince
Calls the `Dump` function for all objects of a type derived from class `CObject` that were allocated (and are still allocated) since the last [Checkpoint](../vs140/CMemoryState--Checkpoint.md) call for this `CMemoryState` object.  
  
## Syntax  
  
```  
  
void DumpAllObjectsSince( ) const;  
```  
  
## Remarks  
 Calling `DumpAllObjectsSince` with an uninitialized `CMemoryState` object will dump out all objects currently in memory.  
  
## Example  
 See the example for the [CMemoryState](../vs140/CMemoryState--CMemoryState.md) constructor.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CMemoryState Structure](../vs140/CMemoryState-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)