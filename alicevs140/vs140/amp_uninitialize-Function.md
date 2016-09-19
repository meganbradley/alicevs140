---
title: "amp_uninitialize Function"
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
ms.assetid: 6e6844b9-129f-4543-9c1c-e18e10c1d408
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# amp_uninitialize Function
Uninitializes the C++ AMP runtime. It is legal to call this function multiple times during an applications lifetime. Calling any C++ AMP API afer calling this function will reinitialize the C++ AMP runtime. Note that it is illegal to use C++ AMP objects across calls to this function and doing so will result in undefined behavior. Also, concurrently calling this function and any other AMP APIs is illegal and would result in undefined behavior.  
  
## Syntax  
  
```  
void __cdecl amp_uninitialize();  
```  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace (C++ AMP)](../vs140/Concurrency-Namespace--C---AMP-.md)