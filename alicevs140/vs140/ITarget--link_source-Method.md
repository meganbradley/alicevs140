---
title: "ITarget::link_source Method"
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
ms.assetid: 290d6373-a589-4211-a571-3d576b47642d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITarget::link_source Method
When overridden in a derived class, links a specified source block to this `ITarget` block.  
  
## Syntax  
  
```  
virtual void link_source(  
   _Inout_ ISource<_Type> * _PSource  
) = 0;  
```  
  
#### Parameters  
 `_PSource`  
 The `ISource` block being linked to this `ITarget` block.  
  
## Remarks  
 This function should not be called directly on an `ITarget` block. Blocks should be connected together using the `link_target` method on `ISource` blocks, which will invoke the `link_source` method on the corresponding target.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ITarget Class](../vs140/ITarget-Class.md)