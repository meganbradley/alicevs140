---
title: "Async.CancellationToken Property (F#)"
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
  - Async.CancellationToken
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 3f118642-dd42-4e34-9a63-1779e7a0a6f9
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Async.CancellationToken Property (F#)
Creates an asynchronous computation that returns the cancellation token governing the execution of the computation.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member CancellationToken :  Async<CancellationToken>  
  
// Usage:  
Async.CancellationToken  
```  
  
## Return Value  
 An asynchronous computation capable of retrieving the <xref:System.Threading.CancellationToken?qualifyHint=False> from a computation expression.  
  
## Remarks  
 In an asynchronous computation such as the following, a cancellation token can be used to initiate other asynchronous operations that will cancel cooperatively with this workflow.  
  
```f#  
async { let! token = Async.CancellationToken ...}  
```  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Async Class (F#)](../Topic/Control.Async%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)