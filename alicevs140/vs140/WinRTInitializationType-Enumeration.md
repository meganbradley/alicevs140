---
title: "WinRTInitializationType Enumeration"
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
ms.assetid: adcbbd85-2622-45a8-983e-3718dabbb902
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WinRTInitializationType Enumeration
Used by the `WinRTInitialization` policy to describe whether and how the Windows Runtime will be initialized on scheduler threads for an application which runs on operating systems with version Windows 8 or higher. For more information on available scheduler policies, see [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md).  
  
## Syntax  
  
```  
enum WinRTInitializationType;  
```  
  
## Members  
  
### Values  
  
|Name|Description|  
|----------|-----------------|  
|`DoNotInitializeWinRT`|When the application is run on operating systems with version Windows 8 or higher, threads within the scheduler will not initialize the Windows Runtime .|  
|`InitializeWinRTAsMTA`|When the application is run on operating systems with version Windows 8 or higher, each thread within the scheduler will initialize the Windows Runtime and declare that it is part of the multithreaded apartment.|  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)