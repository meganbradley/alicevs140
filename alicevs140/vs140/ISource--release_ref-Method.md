---
title: "ISource::release_ref Method"
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
ms.assetid: fff8ee3f-404a-4c67-8572-b60777b2de34
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ISource::release_ref Method
When overridden in a derived class, releases a reference count on this `ISource` block.  
  
## Syntax  
  
```  
virtual void release_ref(  
   _Inout_ ITarget<_Type> * _PTarget  
) = 0;  
```  
  
#### Parameters  
 `_PTarget`  
 A pointer to the target block that is calling this method.  
  
## Remarks  
 This method is called by an `ITarget` object that is being unlinked from this source. The source block is allowed to release any resources reserved for the target block.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ISource Class](../vs140/ISource-Class.md)