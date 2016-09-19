---
title: "choice::unlink_target Method"
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
ms.assetid: 0fd72322-9434-4033-9580-c287da042b1a
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# choice::unlink_target Method
Unlinks a target block from this `choice` messaging block.  
  
## Syntax  
  
```  
virtual void unlink_target(  
   _Inout_ ITarget<size_t> * _PTarget  
);  
```  
  
#### Parameters  
 `_PTarget`  
 A pointer to an `ITarget` block to unlink from this `choice` messaging block.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [choice Class](../vs140/choice-Class.md)