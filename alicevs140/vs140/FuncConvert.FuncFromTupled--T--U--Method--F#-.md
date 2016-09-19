---
title: "FuncConvert.FuncFromTupled&lt;&#39;T,&#39;U&gt; Method (F#)"
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
apiname: 
  - FuncConvert.FuncFromTupled<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 687a5ec4-0dff-414e-ab4a-84666580a608
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FuncConvert.FuncFromTupled&lt;&#39;T,&#39;U&gt; Method (F#)
A utility function to convert function values from tupled to curried form.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signatures:  
static member FuncConvert.FuncFromTupled : ('T -> 'U) -> 'T -> 'U  
  
// Usage:  
FuncConvert.FuncFromTupled (func)  
```  
  
#### Parameters  
 `func`  
 Type: `'T -> 'U`  
  
## Return Value  
  
## Remarks  
  
## Platforms  
 Windows 7, Windows Vista, Windows XP SP2, Windows Server 2008 R2, Windows Server 2008, Windows Server 2003, Windows Server 2000 SP4  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
 Supported in: 2.0, 3.0  
  
## See Also  
 [Core.FuncConvert Class (F#)](../Topic/Core.FuncConvert%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)