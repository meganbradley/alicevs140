---
title: "FuncConvert.FuncFromTupled&lt;&#39;T1,&#39;T2,&#39;T3,&#39;T4,&#39;U&gt; Method (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 0b0bd5cb-0312-4694-937c-495347eae1d1
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FuncConvert.FuncFromTupled&lt;&#39;T1,&#39;T2,&#39;T3,&#39;T4,&#39;U&gt; Method (F#)
A utility function to convert function values from tupled to curried form.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member FuncFromTupled : ('T1 * 'T2 * 'T3 * 'T4 -> 'U) -> 'T1 -> 'T2 -> 'T3 -> 'T4 -> 'U  
  
// Usage:  
FuncConvert.FuncFromTupled (func)  
```  
  
#### Parameters  
 `func`  
 Type: `'T1 * 'T2 * 'T3 * 'T4 -> 'U`  
  
 The input function that has tupled arguments.  
  
## Return Value  
 The output curried function.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.FuncConvert Class (F#)](../Topic/Core.FuncConvert%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)