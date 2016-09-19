---
title: "AsyncBuilder.While Method (F#)"
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
  - AsyncBuilder.While
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d47c0775-5a40-4e74-a9ae-f96c5385efe7
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AsyncBuilder.While Method (F#)
Implements the `while` keyword in asynchronous computation expressions.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.While : (unit -> bool) * Async<unit> -> Async<unit>  
  
// Usage:  
asyncBuilder.While (guard, computation)  
```  
  
#### Parameters  
 `guard`  
 Type: [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md) `->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to determine when to stop executing `computation`.  
  
 `computation`  
 Type: [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)`>`  
  
 The function to be executed. Equivalent to the body of a `while` expression.  
  
## Return Value  
 An asynchronous computation that behaves similarly to a while loop when run.  
  
## Remarks  
 Creates an asynchronous computation that runs `computation` repeatedly until `guard` evaluates to false.  
  
 A cancellation check is performed whenever the computation is executed. The existence of this method permits the use of `while` in the `async { ... }` computation expression syntax.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.AsyncBuilder Class (F#)](../vs140/Control.AsyncBuilder-Class--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)