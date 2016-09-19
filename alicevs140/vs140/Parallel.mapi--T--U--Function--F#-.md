---
title: "Parallel.mapi&lt;&#39;T,&#39;U&gt; Function (F#)"
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
ms.assetid: 994595e4-6886-467e-a6c3-cebc4e621052
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Parallel.mapi&lt;&#39;T,&#39;U&gt; Function (F#)
Build a new array whose elements are the results of applying the given function to each of the elements of the array. The integer index passed to the function indicates the index of element being transformed.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.ArrayModule.Parallel  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
mapi : (int -> 'T -> 'U) -> 'T [] -> 'U []  
  
// Usage:  
mapi mapping array  
```  
  
#### Parameters  
 `mapping`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T -> 'U`  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 'U[]  
  
## Remarks  
 Performs the operation in parallel using System.Threading.Tasks.Parallel.For. The order in which the given function is applied to elements of the input array is not specified.  
  
 This function is named `MapIndexed` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0  
  
## See Also  
 [Array.Parallel Module (F#)](../vs140/Array.Parallel-Module--F#-.md)   
 [Microsoft.FSharp.Collections.ArrayModule Namespace (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)