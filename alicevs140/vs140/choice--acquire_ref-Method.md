---
title: "choice::acquire_ref Method"
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
ms.assetid: 283bdfb0-2e22-4bdb-a1f8-436a7617535e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# choice::acquire_ref Method
Acquires a reference count on this `choice` messaging block, to prevent deletion.  
  
## Syntax  
  
```  
virtual void acquire_ref(  
   _Inout_ ITarget<size_t> * _PTarget  
);  
```  
  
#### Parameters  
 `_PTarget`  
 A pointer to the target block that is calling this method.  
  
## Remarks  
 This method is called by an `ITarget` object that is being linked to this source during the `link_target` method.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [choice Class](../vs140/choice-Class.md)