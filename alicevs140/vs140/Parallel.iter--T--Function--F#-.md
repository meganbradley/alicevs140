---
title: "Parallel.iter&lt;&#39;T&gt; Function (F#)"
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
ms.assetid: 2484b54a-41b7-482e-8931-b528b32ba93e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Parallel.iter&lt;&#39;T&gt; Function (F#)
Apply the given function to each element of the array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.ArrayModule.Parallel  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
iter : ('T -> unit) -> 'T [] -> unit  
  
// Usage:  
iter action array  
```  
  
#### Parameters  
 `action`  
 Type: `'T ->`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Remarks  
 Performs the operation in parallel using System.Threading.Parallel.For. The order in which the given function is applied to elements of the input array is not specified.  
  
 This function is named `Iterate` in the .NET assembly. If accessing the member from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0  
  
## See Also  
 [Array.Parallel Module (F#)](../vs140/Array.Parallel-Module--F#-.md)   
 [Microsoft.FSharp.Collections.ArrayModule Namespace (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)