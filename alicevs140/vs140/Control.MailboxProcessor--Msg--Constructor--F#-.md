---
title: "Control.MailboxProcessor&lt;&#39;Msg&gt; Constructor (F#)"
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
  - MailboxProcessor.MailboxProcessor<'Msg>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f13a40de-09c2-4446-9465-c1c476c57d1e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control.MailboxProcessor&lt;&#39;Msg&gt; Constructor (F#)
Creates an agent.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
new MailboxProcessor : (MailboxProcessor<'Msg> -> Async<unit>) * ?CancellationToken -> MailboxProcessor<'Msg>  
  
// Usage:  
new MailboxProcessor (body)  
new MailboxProcessor (body, cancellationToken = cancellationToken)  
```  
  
#### Parameters  
 `body`  
 Type: [MailboxProcessor](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md)`<'Msg> ->` [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)`>`  
  
 The function to produce an asynchronous computation that will be executed as the read loop for the [MailboxProcessor](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md) when [Start](../vs140/MailboxProcessor.Start--Msg--Method--F#-.md) is called.  
  
 `cancellationToken`  
 Type: [CancellationToken](../Topic/Threading.CancellationToken%20Structure%20\(F%23\).md)  
  
 An optional cancellation token for the `body`. Defaults to [Async.DefaultCancellationToken](../Topic/Async.DefaultCancellationToken%20Property%20\(F%23\).md).  
  
## Return Value  
 The created MailboxProcessor.  
  
## Remarks  
 The `body` function is used to generate the asynchronous computation executed by the agent. This function is not executed until [Start](../vs140/MailboxProcessor.Start--Msg--Method--F#-.md) is called.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.MailboxProcessor<'Msg> Class (F#)](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)