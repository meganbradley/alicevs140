---
title: "PogoSafeMode"
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
ms.assetid: 2daeeff7-44cb-417f-90eb-6b9edf658533
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PogoSafeMode
Specify whether to use fast mode or safe mode for application profiling.  
  
## Syntax  
  
```  
PogoSafeMode  
```  
  
## Remarks  
 Profile-guided optimization (PGO) has two possible modes during the profiling phase: fast mode and safe mode. When profiling is in fast mode, it uses the **INC** instruction to increase data counters. The **INC** instruction is faster but is not thread-safe. When profiling is in safe mode, it uses the **LOCK INC** instruction to increase data counters. The **LOCK INC** instruction has the same functionality as the **INC** instruction has, and is thread-safe, but it is slower than the **INC** instruction.  
  
 By default, PGO profiling operates in fast mode. `PogoSafeMode` is only required if you want to use safe mode.  
  
 To run PGO profiling in safe mode, you must either use the environment variable `PogoSafeMode` or the linker switch **-PogoSafeMode**, depending on the system. If you are performing the profiling on an x64 computer, you must use the linker switch. If you are performing the profiling on an x86 computer, you must define the environment variable to any value before you start the optimization process.  
  
## Example  
  
```  
set PogoSafeMode=1  
```  
  
## See Also  
 [Environment Variables for Profile-Guided Optimizations](../vs140/Environment-Variables-for-Profile-Guided-Optimizations.md)   
 [Profile-Guided Optimizations](../vs140/Profile-Guided-Optimizations.md)