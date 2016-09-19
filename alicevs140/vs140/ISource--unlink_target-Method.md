---
title: "ISource::unlink_target Method"
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
ms.assetid: 90022aa3-56f7-4ada-9078-4d05721bbbd1
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ISource::unlink_target Method
When overridden in a derived class, unlinks a target block from this `ISource` block, if found to be previously linked.  
  
## Syntax  
  
```  
virtual void unlink_target(  
   _Inout_ ITarget<_Type> * _PTarget  
) = 0;  
```  
  
#### Parameters  
 `_PTarget`  
 A pointer to the target block being unlinked from this `ISource` block.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ISource Class](../vs140/ISource-Class.md)