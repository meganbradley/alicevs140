---
title: "DisableTracing Function"
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
ms.assetid: deccd704-c8de-4026-81e9-9214dbb5d71e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DisableTracing Function
Disables tracing in the Concurrency Runtime. This function is deprecated because ETW tracing is unregistered by default.  
  
## Syntax  
  
```  
__declspec(  
   deprecated("Concurrency::DisableTracing is a deprecated function.")  
) _CRTIMP HRESULT __cdecl DisableTracing();  
```  
  
## Return Value  
 If tracing was correctly disabled, `S_OK` is returned. If tracing was not previously initiated, `E_NOT_STARTED` is returned  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)