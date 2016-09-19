---
title: "Array.iter&lt;&#39;T&gt; Function (F#)"
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
  - Array.iter<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 94eba0f1-ecd7-459f-b89f-ed2a2923e516
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.iter&lt;&#39;T&gt; Function (F#)
Applies the given function to each element of the array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.iter : ('T -> unit) -> 'T [] -> unit  
  
// Usage:  
Array.iter action array  
```  
  
#### Parameters  
 `action`  
 Type: `'T ->` [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 The function to apply.  
  
 `array`  
 Type: `'T` [&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Remarks  
 This function is named `Iterate` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code demonstrates the use of `Array.iter`.  
  
 [!CODE [FsSamples101#1002](../CodeSnippet/VS_Snippets_Fsharp/fssamples101#1002)]  
  
 **Array.iter: (1, 1) (2, 4) (3, 9) (4, 16) (5, 25)**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)