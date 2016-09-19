---
title: "GetProcessorNodeCount Function"
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
ms.assetid: ffbc9395-d79c-4cb4-bbb3-8511820f5c62
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetProcessorNodeCount Function
Returns the number of NUMA nodes or processor packages on the underlying system.  
  
## Syntax  
  
```  
unsigned int __cdecl GetProcessorNodeCount();  
```  
  
## Return Value  
 The number of NUMA nodes or processor packages.  
  
## Remarks  
 If the system contains more NUMA nodes than processor packages, the number of NUMA nodes is returned, otherwise, the number of processor packages is returned.  
  
 [unsupported_os](../vs140/unsupported_os-Class.md) is thrown if the operating system is not supported by the Concurrency Runtime.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [IResourceManager::OSVersion Enumeration](../vs140/IResourceManager--OSVersion-Enumeration.md)