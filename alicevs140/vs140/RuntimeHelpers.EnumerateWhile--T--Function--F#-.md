---
title: "RuntimeHelpers.EnumerateWhile&lt;&#39;T&gt; Function (F#)"
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
  - RuntimeHelpers.EnumerateWhile<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 9f48435f-2754-42e2-8d1a-9d002b7e60b5
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RuntimeHelpers.EnumerateWhile&lt;&#39;T&gt; Function (F#)
The F# compiler emits calls to this function to implement the `while` keyword for F# sequence expressions.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.CompilerServices.RuntimeHelpers  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RuntimeHelpers.EnumerateWhile : (unit -> bool) -> seq<'T> -> seq<'T>  
  
// Usage:  
RuntimeHelpers.EnumerateWhile guard source  
```  
  
#### Parameters  
 `guard`  
 Type: [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md) `->` [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 A function that indicates whether iteration should continue.  
  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input sequence.  
  
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