---
title: "MailboxProcessor.Scan&lt;&#39;Msg,&#39;T&gt; Method (F#)"
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
  - MailboxProcessor.Scan<'Msg,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e86368a3-4f97-4b51-a487-4c6b5456fcbe
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MailboxProcessor.Scan&lt;&#39;Msg,&#39;T&gt; Method (F#)
Scans for a message by looking through messages in arrival order until a provided function returns a `Some` value. Other messages remain in the queue.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Scan : ('Msg -> Async<'T> option) * ?int -> Async<'T>  
  
// Usage:  
mailboxProcessor.Scan (scanner)  
mailboxProcessor.Scan (scanner, timeout = timeout)  
```  
  
#### Parameters  
 `scanner`  
 Type: `'Msg ->` [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<'T>` [option](../vs140/Core.Option--T--Union--F#-.md)  
  
 A function that returns `None` if the message is to be skipped, or `Some` if the message is to be processed and removed from the queue.  
  
 `timeout`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 An optional timeout in milliseconds. Defaults to -1 which corresponds to <xref:System.Threading.Timeout.Infinite?qualifyHint=False>.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.TimeoutException?qualifyHint=False>|Thrown when the timeout is exceeded.|  
  
## Return Value  
 An asynchronous computation ([Async](../Topic/Control.Async%20Class%20\(F%23\).md) object) that `scanner` built off the read message.  
  
## Remarks  
 This method is for use within the body of the agent. For each agent, at most one concurrent reader may be active, so no more than one concurrent call to [Receive](../vs140/MailboxProcessor.Receive--Msg--Method--F#-.md), [TryReceive](../Topic/MailboxProcessor.TryReceive%3C'Msg%3E%20Method%20\(F%23\).md), `Scan` or [TryScan](../Topic/MailboxProcessor.TryScan%3C'Msg,'T%3E%20Method%20\(F%23\).md) may be active. The body of the `scanner` function is locked during its execution, but the lock is released before the execution of the asynchronous workflow.  
  
## Example  
 The following example shows how to use the `Scan` method. In this code, mailbox processor agents manage a series of simulated jobs that run and compute a result.  
  
 [!CODE [FsMailboxProcessor#21](../CodeSnippet/VS_Snippets_Fsharp/fsmailboxprocessor#21)]  
  
 A sample session follows.  
  
 **Number Of Logical Processors: 2Requesting job #1Job #1 submitted.Job #1 started on procId 0.Requesting job #2Job #2 submitted.Job #2 started on procId 1.Requesting job #3Requesting job #4Requesting job #5Requesting job #6Requesting job #7Requesting job #8Requesting job #9Requesting job #10Job #1 completed.Nth Prime for N = 5000 is 48611.Job #3 submitted.Job #3 started on procId 0.Done submitting jobs. Press Enter to exit when ready.Job #2 completed.Nth Prime for N = 10000 is 104729.Job #4 submitted.Job #4 started on procId 1.Job #3 completed.Nth Prime for N = 15000 is 163841.Job #5 submitted.Job #5 started on procId 0.Job #4 completed.Nth Prime for N = 20000 is 224737.Job #6 submitted.Job #6 started on procId 1.Job #5 completed.Nth Prime for N = 25000 is 287117.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.MailboxProcessor<'Msg> Class (F#)](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)