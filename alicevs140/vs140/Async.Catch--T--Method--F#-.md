---
title: "Async.Catch&lt;&#39;T&gt; Method (F#)"
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
  - Async.Catch<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c31e1ccb-c0f5-4da9-ba3d-c2454bcd0807
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Async.Catch&lt;&#39;T&gt; Method (F#)
Creates an asynchronous computation that executes a specified computation. If this computation completes successfully, then this method returns `Choice1Of2` with the returned value. If this computation raises an exception before it completes then return `Choice2Of2` with the raised exception.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member Catch : Async<'T> -> Async<Choice<'T,exn>>  
  
// Usage:  
Async.Catch (computation)  
```  
  
#### Parameters  
 `computation`  
 Type: [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<'T>`  
  
 The input computation that returns the type 'T.  
  
## Return Value  
 A computation that returns a [Choice](../vs140/Core.Choice--T1--T2--Union--F#-.md) of type 'T or an exception.  
  
## Remarks  
  
## Example  
 The following code example shows how to use `Async.Catch` to run an asynchronous computation that might throw an exception.  
  
 [!CODE [FsAsyncAPIs#18](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis#18)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Async Class (F#)](../Topic/Control.Async%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)