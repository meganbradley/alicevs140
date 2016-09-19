---
title: "Register Usage"
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
ms.assetid: ce58e2cf-afd3-4068-980e-28a209298265
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Register Usage
The [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)] architecture provides for 16 general-purpose registers (hereafter referred to as integer registers) as well as 16 XMM/YMM registers available for floating-point use. Volatile registers are scratch registers presumed by the caller to be destroyed across a call. Nonvolatile registers are required to retain their values across a function call and must be saved by the callee if used.  
  
 The following table describes how each register is used across function calls:  
  
||||  
|-|-|-|  
|Register|Status|Use|  
|RAX|Volatile|Return value register|  
|RCX|Volatile|First integer argument|  
|RDX|Volatile|Second integer argument|  
|R8|Volatile|Third integer argument|  
|R9|Volatile|Fourth integer argument|  
|R10:R11|Volatile|Must be preserved as needed by caller; used in syscall/sysret instructions|  
|R12:R15|Nonvolatile|Must be preserved by callee|  
|RDI|Nonvolatile|Must be preserved by callee|  
|RSI|Nonvolatile|Must be preserved by callee|  
|RBX|Nonvolatile|Must be preserved by callee|  
|RBP|Nonvolatile|May be used as a frame pointer; must be preserved by callee|  
|RSP|Nonvolatile|Stack pointer|  
|XMM0, YMM0|Volatile|First FP argument; first vector-type argument when `__vectorcall` is used|  
|XMM1, YMM1|Volatile|Second FP argument; second vector-type argument when `__vectorcall` is used|  
|XMM2, YMM2|Volatile|Third FP argument; third vector-type argument when `__vectorcall` is used|  
|XMM3, YMM3|Volatile|Fourth FP argument; fourth vector-type argument when `__vectorcall` is used|  
|XMM4, YMM4|Volatile|Must be preserved as needed by caller; fifth vector-type argument when `__vectorcall` is used|  
|XMM5, YMM5|Volatile|Must be preserved as needed by caller; sixth vector-type argument when `__vectorcall` is used|  
|XMM6:XMM15, YMM6:YMM15|Nonvolatile (XMM), Volatile (upper half of YMM)|Must be preserved as needed by callee. YMM registers must be preserved as needed by caller.|  
  
## See Also  
 [x64 Software Conventions](../vs140/x64-Software-Conventions.md)   
 [__vectorcall](../vs140/__vectorcall.md)