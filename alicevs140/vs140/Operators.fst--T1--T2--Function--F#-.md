---
title: "Operators.fst&lt;&#39;T1,&#39;T2&gt; Function (F#)"
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
  - Operators.fst<'T1,'T2>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: da3d2f84-1907-45a6-95be-0b1325c9be71
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.fst&lt;&#39;T1,&#39;T2&gt; Function (F#)
Return the first element of a tuple, `fst (a,b) = a`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
fst : 'T1 * 'T2 -> 'T1  
  
// Usage:  
fst tuple  
```  
  
#### Parameters  
 `tuple`  
 Type: `'T1 * 'T2`  
  
 The input tuple.  
  
## Return Value  
 The first value.  
  
## Remarks  
 This function is named `Fst` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)