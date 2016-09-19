---
title: "MailboxProcessor.Start&lt;&#39;Msg&gt; Method (F#)"
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
  - MailboxProcessor.Start<'Msg>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ebf18bf3-ba17-42b9-91ac-313a7eee6fa0
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MailboxProcessor.Start&lt;&#39;Msg&gt; Method (F#)
Creates and starts an agent.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member Start : (MailboxProcessor<'Msg> -> Async<unit>) * ?CancellationToken -> MailboxProcessor<'Msg>  
  
// Usage:  
MailboxProcessor.Start (body)  
MailboxProcessor.Start (body, cancellationToken = cancellationToken)  
```  
  
#### Parameters  
 `body`  
 Type: [MailboxProcessor](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md)`<'Msg> ->` [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)`>`  
  
 The function to produce an asynchronous computation that will be executed as the read loop for the [MailboxProcessor](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md) when `Start` is called.  
  
 `cancellationToken`  
 Type: [CancellationToken](../Topic/Threading.CancellationToken%20Structure%20\(F%23\).md)  
  
 An optional cancellation token for the `body`. The default is [Async.DefaultCancellationToken](../Topic/Async.DefaultCancellationToken%20Property%20\(F%23\).md).  
  
## Return Value  
 The created [MailboxProcessor](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md).  
  
## Remarks  
 The `body` function is used to generate the asynchronous computation executed by the agent.  
  
## Example  
 The following code example shows how to start a mailbox processor agent. In this example, each line of input from the console is posted to a message queue. The program reads each message and replies by using a reply channel. When the special message "Stop" is received, the Stop reply is sent and the program exits.  
  
 [!CODE [FsMailboxProcessor#7](../CodeSnippet/VS_Snippets_Fsharp/fsmailboxprocessor#7)]  
  
 Following is an example session.  
  
 **Mailbox Processor TestType some text and press Enter to submit a message.Type 'Stop' to close the program.> hello1 : Console loop4 : mailboxProcessorReply: Message number 0 was received. Message contents: hello> testing1 : Console loop3 : mailboxProcessorReply: Message number 1 was received. Message contents: testing> hello?1 : Console loop4 : mailboxProcessorReply: Message number 2 was received. Message contents: hello?> testing 1 2 31 : Console loop3 : mailboxProcessorReply: Message number 3 was received. Message contents: testing 1 2 3> Stop1 : Console loop4 : mailboxProcessorPress Enter to continue.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.MailboxProcessor<'Msg> Class (F#)](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)