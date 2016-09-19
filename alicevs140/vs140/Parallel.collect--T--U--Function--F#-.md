---
title: "Parallel.collect&lt;&#39;T,&#39;U&gt; Function (F#)"
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
ms.assetid: 3787e401-d84e-4521-9d7f-87303753dc7b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Parallel.collect&lt;&#39;T,&#39;U&gt; Function (F#)
For each element of the array, apply the given function. Concatenate all the results and return the combined array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.ArrayModule.Parallel  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
collect : ('T -> 'U []) -> 'T [] -> 'U []  
  
// Usage:  
collect mapping array  
```  
  
#### Parameters  
 `mapping`  
 Type: `'T -> 'U`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The array of concatenated results.  
  
## Remarks  
 Performs the operation in parallel using System.Threading.Tasks.Parallel.For. The order in which the given function is applied to elements of the input array is not specified.  
  
 This function is named `Collect` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0  
  
## See Also  
 [Array.Parallel Module (F#)](../vs140/Array.Parallel-Module--F#-.md)   
 [Microsoft.FSharp.Collections.ArrayModule Namespace (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)