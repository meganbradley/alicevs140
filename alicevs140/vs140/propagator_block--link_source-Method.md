---
title: "propagator_block::link_source Method"
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
ms.assetid: e253fa95-03c8-4ef3-80f4-4459fc1e8a2a
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# propagator_block::link_source Method
Links a specified source block to this `propagator_block` object.  
  
## Syntax  
  
```  
virtual void link_source(  
   _Inout_ ISource<_Source_type> * _PSource  
);  
```  
  
#### Parameters  
 `_PSource`  
 A pointer to the `ISource` block that is to be linked.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [propagator_block Class](../vs140/propagator_block-Class.md)