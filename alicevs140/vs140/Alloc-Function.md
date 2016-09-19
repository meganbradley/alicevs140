---
title: "Alloc Function"
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
ms.assetid: 41246453-c699-4a73-9234-f952efbd9106
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Alloc Function
Allocates a block of memory of the size specified from the Concurrency Runtime Caching Suballocator.  
  
## Syntax  
  
```  
void * __cdecl Alloc(  
   size_t _NumBytes  
);  
```  
  
#### Parameters  
 `_NumBytes`  
 The number of bytes of memory to allocate.  
  
## Return Value  
 A pointer to newly allocated memory.  
  
## Remarks  
 For more information about which scenarios in your application could benefit from using the Caching Suballocator, see [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md).  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [Concurrency::Free Function](../vs140/Free-Function.md)