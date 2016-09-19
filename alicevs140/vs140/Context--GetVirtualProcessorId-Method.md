---
title: "Context::GetVirtualProcessorId Method"
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
ms.assetid: b5ebe25c-faca-4e33-a6b9-a5fde676123e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::GetVirtualProcessorId Method
Returns an identifier for the virtual processor that the context is currently executing on.  
  
## Syntax  
  
```  
virtual unsigned int GetVirtualProcessorId() const =0;  
```  
  
## Return Value  
 If the context is currently executing on a virtual processor, an identifier for the virtual processor that the context is currently executing on; otherwise, the value `-1`.  
  
## Remarks  
 The return value from this method is an instantaneous sampling of the virtual processor that the context is executing on. This value can be stale the moment it is returned and cannot be relied upon. Typically, this method is used for debugging or tracing purposes only.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)