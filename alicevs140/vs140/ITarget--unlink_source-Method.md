---
title: "ITarget::unlink_source Method"
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
ms.assetid: f3841a19-f009-4749-9270-e51834d60589
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITarget::unlink_source Method
When overridden in a derived class, unlinks a specified source block from this `ITarget` block.  
  
## Syntax  
  
```  
virtual void unlink_source(  
   _Inout_ ISource<_Type> * _PSource  
) = 0;  
```  
  
#### Parameters  
 `_PSource`  
 The `ISource` block being unlinked from this `ITarget` block.  
  
## Remarks  
 This function should not be called directly on an `ITarget` block. Blocks should be disconnected using the `unlink_target` or `unlink_targets` methods on `ISource` blocks, which will invoke the `unlink_source` method on the corresponding target.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ITarget Class](../vs140/ITarget-Class.md)