---
title: "GetOSVersion Function"
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
ms.assetid: 73388a52-9b59-42d6-a49b-d35856fa671a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetOSVersion Function
Returns the operating system version.  
  
## Syntax  
  
```  
IResourceManager::OSVersion __cdecl GetOSVersion();  
```  
  
## Return Value  
 An enumerated value representing the operating system.  
  
## Remarks  
 [unsupported_os](../vs140/unsupported_os-Class.md) is thrown if the operating system is not supported by the Concurrency Runtime.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [IResourceManager::OSVersion Enumeration](../vs140/IResourceManager--OSVersion-Enumeration.md)