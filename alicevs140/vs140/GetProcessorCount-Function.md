---
title: "GetProcessorCount Function"
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
ms.assetid: bea5a723-89bf-4597-8657-46ecff3f0fae
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetProcessorCount Function
Returns the number of hardware threads on the underlying system.  
  
## Syntax  
  
```  
unsigned int __cdecl GetProcessorCount();  
```  
  
## Return Value  
 The number of hardware threads.  
  
## Remarks  
 [unsupported_os](../vs140/unsupported_os-Class.md) is thrown if the operating system is not supported by the Concurrency Runtime.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [IResourceManager::OSVersion Enumeration](../vs140/IResourceManager--OSVersion-Enumeration.md)