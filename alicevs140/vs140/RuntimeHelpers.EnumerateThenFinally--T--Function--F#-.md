---
title: "RuntimeHelpers.EnumerateThenFinally&lt;&#39;T&gt; Function (F#)"
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
  - RuntimeHelpers.EnumerateThenFinally<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8d9fe619-a247-4de1-9cc8-a0f54517cef6
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RuntimeHelpers.EnumerateThenFinally&lt;&#39;T&gt; Function (F#)
The F# compiler emits calls to this function to implement the `try...finally` construct for F# sequence expressions.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.CompilerServices.RuntimeHelpers  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RuntimeHelpers.EnumerateThenFinally : seq<'T> -> (unit -> unit) -> seq<'T>  
  
// Usage:  
RuntimeHelpers.EnumerateThenFinally source compensation  
```  
  
#### Parameters  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input sequence.  
  
 `compensation`  
 Type: [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md) `->` [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 A computation to be included in an enumerator's Dispose method.  
  
## Return Value  
 The result sequence.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [CompilerServices.RuntimeHelpers Module (F#)](../Topic/CompilerServices.RuntimeHelpers%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core.CompilerServices Namespace (F#)](../vs140/Microsoft.FSharp.Core.CompilerServices-Namespace--F#-.md)