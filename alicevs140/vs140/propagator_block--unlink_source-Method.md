---
title: "propagator_block::unlink_source Method"
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
ms.topic: article
ms.assetid: ce7bb6fb-914e-47e0-b898-5d27b2257e2a
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# propagator_block::unlink_source Method
Unlinks a specified source block from this `propagator_block` object.  
  
## Syntax  
  
```  
virtual void unlink_source(  
   _Inout_ ISource<_Source_type> * _PSource  
);  
```  
  
#### Parameters  
 `_PSource`  
 A pointer to the `ISource` block that is to be unlinked.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [propagator_block Class](../vs140/propagator_block-Class.md)