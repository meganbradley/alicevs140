---
title: "AsyncBuilder.ReturnFrom&lt;&#39;T&gt; Method (F#)"
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
  - AsyncBuilder.ReturnFrom<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f76f8b91-f194-42aa-90e9-ca26650baef2
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AsyncBuilder.ReturnFrom&lt;&#39;T&gt; Method (F#)
Implements the `return!` keyword for asynchronous computations. This function delegates to the input computation.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.ReturnFrom : Async<'T> -> Async<'T>  
  
// Usage:  
asyncBuilder.ReturnFrom (computation)  
```  
  
#### Parameters  
 `computation`  
 Type: [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<'T>`  
  
 The input computation.  
  
## Return Value  
 The input computation.  
  
## Remarks  
 The existence of this method permits the use of `return!` in the `async { ... }` computation expression syntax.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.AsyncBuilder Class (F#)](../vs140/Control.AsyncBuilder-Class--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)