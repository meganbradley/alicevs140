---
title: "Async.StartAsTask&lt;&#39;T&gt; Method (F#)"
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
ms.assetid: 3f3ef301-fcc9-4006-9414-c2268e65d79c
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Async.StartAsTask&lt;&#39;T&gt; Method (F#)
Executes a computation in the thread pool. Returns a <xref:System.Threading.Tasks.Task?qualifyHint=False> that will be completed in the corresponding state once the computation terminates (produces the result, throws exception or gets canceled) If no cancellation token is provided then the default cancellation token is used.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member StartAsTask : Async<'T> * ?TaskCreationOptions * ?CancellationToken -> Task<'T>  
  
// Usage:  
Async.StartAsTask (computation)  
Async.StartAsTask (computation, taskCreationOptions = taskCreationOptions, cancellationToken = cancellationToken)  
```  
  
#### Parameters  
 `computation`  
 Type: [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<'T>`  
  
 The computation to execute.  
  
 `taskCreationOptions`  
 Type: <xref:System.Threading.Tasks.TaskCreationOptions?qualifyHint=False>  
  
 Optional task creation options.  
  
 `cancellationToken`  
 Type: <xref:System.Threading.CancellationToken?qualifyHint=False>  
  
 Optional cancellation token.  
  
## Return Value  
 A <xref:System.Threading.Tasks.Task`1?qualifyHint=False> object that represents the given computation.  
  
## Remarks  
  
## Example  
 The following code example demonstrates the use of `Async.StartAsTask`.  
  
 [!CODE [FsAsyncAPIs#330](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis#330)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Control.Async Class (F#)](../Topic/Control.Async%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)