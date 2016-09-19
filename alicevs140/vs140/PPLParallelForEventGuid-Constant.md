---
title: "PPLParallelForEventGuid Constant"
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
ms.assetid: db0a6329-840f-4db5-8f84-1f531d9cc382
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PPLParallelForEventGuid Constant
A category GUID describing ETW events fired by the Concurrency Runtime that are directly related to usage of the `parallel_for` function.  
  
## Syntax  
  
```  
const __declspec(selectany) GUID PPLParallelForEventGuid = { 0x31c8da6b, 0x6165, 0x4042, { 0x8b, 0x92, 0x94, 0x9e, 0x31, 0x5f, 0x4d, 0x84 } };  
```  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [parallel_for Function](../vs140/parallel_for-Function.md)