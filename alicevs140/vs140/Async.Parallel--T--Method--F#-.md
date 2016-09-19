---
title: "Async.Parallel&lt;&#39;T&gt; Method (F#)"
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
  - Async.Parallel<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: aa9b0355-2d55-4858-b943-cbe428de9dc4
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Async.Parallel&lt;&#39;T&gt; Method (F#)
Creates an asynchronous computation that executes all the given asynchronous computations, initially queueing each as work items and using a fork/join pattern.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member Parallel : seq<Async<'T>> -> Async<'T []>  
  
// Usage:  
Async.Parallel (computations)  
```  
  
#### Parameters  
 `computations`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<`[Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<'T>>`  
  
 A sequence of distinct computations to be parallelized.  
  
## Return Value  
 A computation that returns an array of values from the sequence of input computations.  
  
## Remarks  
 If all child computations succeed, an array of results is passed to the success continuation. If any child computation raises an exception, then the overall computation will trigger an exception, and cancel the others. The overall computation will respond to cancellation while executing the child computations. If cancelled, the computation will cancel any remaining child computations but will still wait for the other child computations to complete.  
  
## Example  
 The following code example shows how to use `Async.Parallel` to run computations that write to a number of files asynchronously.  
  
 [!CODE [FsAsyncAPIs#32](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis#32)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Async Class (F#)](../Topic/Control.Async%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)