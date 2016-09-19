---
title: "EnableTracing Function"
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
ms.assetid: 66ece37f-97f1-490f-bd78-d5ff1e43b805
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EnableTracing Function
Enables tracing in the Concurrency Runtime. This function is deprecated because ETW tracing is now on by default.  
  
## Syntax  
  
```  
__declspec(  
   deprecated("Concurrency::EnableTracing is a deprecated function.")  
) _CRTIMP HRESULT __cdecl EnableTracing();  
```  
  
## Return Value  
 If tracing was correctly initiated, `S_OK` is returned; otherwise, `E_NOT_STARTED` is returned.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)