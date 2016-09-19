---
title: "Control.MailboxProcessor&lt;&#39;Msg&gt; Class (F#)"
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
  - Control.MailboxProcessor<'Msg>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2052c977-f787-4a0b-b25f-9444e26b5fdf
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control.MailboxProcessor&lt;&#39;Msg&gt; Class (F#)
A message-processing agent which executes an asynchronous computation.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<Sealed>]  
[<AutoSerializable(false)>]  
type MailboxProcessor<'Msg> =  
 class  
  interface IDisposable  
  new MailboxProcessor : (MailboxProcessor<'Msg> -> Async<unit>) * ?CancellationToken -> MailboxProcessor<'Msg>  
  member this.Post : 'Msg -> unit  
  member this.PostAndAsyncReply : (AsyncReplyChannel<'Reply> -> 'Msg) * int option -> Async<'Reply>  
  member this.PostAndReply : (AsyncReplyChannel<'Reply> -> 'Msg) * int option -> 'Reply  
  member this.PostAndTryAsyncReply : (AsyncReplyChannel<'Reply> -> 'Msg) * ?int -> Async<'Reply option>  
  member this.Receive : ?int -> Async<'Msg>  
  member this.Scan : ('Msg -> Async<'T> option) * ?int -> Async<'T>  
  member this.Start : unit -> unit  
  static member Start : (MailboxProcessor<'Msg> -> Async<unit>) * ?CancellationToken -> MailboxProcessor<'Msg>  
  member this.TryPostAndReply : (AsyncReplyChannel<'Reply> -> 'Msg) * ?int -> 'Reply option  
  member this.TryReceive : ?int -> Async<'Msg option>  
  member this.TryScan : ('Msg -> Async<'T> option) * ?int -> Async<'T option>  
  member this.add_Error : Handler<Exception> -> unit  
  member this.CurrentQueueLength :  int  
  member this.DefaultTimeout :  int with get, set  
  member this.Error :  IEvent<Exception>  
  member this.remove_Error : Handler<Exception> -> unit  
 end  
```  
  
## Remarks  
 The agent encapsulates a message queue that supports multiple-writers and a single reader agent. Writers send messages to the agent by using the Post method and its variations. The agent may wait for messages using the Receive or TryReceive methods or scan through all available messages using the Scan or TryScan method.  
  
 This type is named `FSharpMailboxProcessor` in the .NET assembly. If accessing the type from a .NET language other than F#, or through reflection, use this name.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Control.MailboxProcessor--Msg--Constructor--F#-.md)|Creates an agent. The `body` function is used to generate the asynchronous computation executed by the agent. This function is not executed until `Start` is called.|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[add_Error](../vs140/MailboxProcessor.add_Error--Msg--Method--F#-.md)|Occurs when the execution of the agent results in an exception.|  
|[CurrentQueueLength](../vs140/MailboxProcessor.CurrentQueueLength--Msg--Property--F#-.md)|Returns the number of unprocessed messages in the message queue of the agent.|  
|[DefaultTimeout](../vs140/MailboxProcessor.DefaultTimeout--Msg--Property--F#-.md)|Raises a timeout exception if a message not received in this amount of time. By default no timeout is used.|  
|[Error](../vs140/MailboxProcessor.Error--Msg--Property--F#-.md)|Occurs when the execution of the agent results in an exception.|  
|[Post](../vs140/MailboxProcessor.Post--Msg--Method--F#-.md)|Posts a message to the message queue of the MailboxProcessor, asynchronously.|  
|[PostAndAsyncReply](../vs140/MailboxProcessor.PostAndAsyncReply--Msg--Reply--Method--F#-.md)|Posts a message to an agent and await a reply on the channel, asynchronously.|  
|[PostAndReply](../vs140/MailboxProcessor.PostAndReply--Msg--Reply--Method--F#-.md)|Posts a message to an agent and await a reply on the channel, synchronously.|  
|[PostAndTryAsyncReply](../vs140/MailboxProcessor.PostAndTryAsyncReply--Msg--Reply--Method--F#-.md)|Like AsyncPostAndReply, but returns None if no reply within the timeout period.|  
|[Receive](../vs140/MailboxProcessor.Receive--Msg--Method--F#-.md)|Waits for a message. This will consume the first message in arrival order.|  
|[remove_Error](../vs140/MailboxProcessor.remove_Error--Msg--Method--F#-.md)|Occurs when the execution of the agent results in an exception.|  
|[Scan](../vs140/MailboxProcessor.Scan--Msg--T--Method--F#-.md)|Scans for a message by looking through messages in arrival order until `scanner` returns a Some value. Other messages remain in the queue.|  
|[Start](../vs140/MailboxProcessor.Start--Msg--Method--F#-.md)|Starts the agent.|  
|[TryPostAndReply](../Topic/MailboxProcessor.TryPostAndReply%3C'Msg,'Reply%3E%20Method%20\(F%23\).md)|Like PostAndReply, but returns None if no reply within the timeout period.|  
|[TryReceive](../Topic/MailboxProcessor.TryReceive%3C'Msg%3E%20Method%20\(F%23\).md)|Waits for a message. This will consume the first message in arrival order.|  
|[TryScan](../Topic/MailboxProcessor.TryScan%3C'Msg,'T%3E%20Method%20\(F%23\).md)|Scans for a message by looking through messages in arrival order until `scanner` returns a Some value. Other messages remain in the queue.|  
  
## Static Members  
  
|Member|Description|  
|------------|-----------------|  
|[Start](../vs140/MailboxProcessor.Start--Msg--Method--F#-.md)|Creates and starts an agent. The `body` function is used to generate the asynchronous computation executed by the agent.|  
  
## Example  
 The following example shows the basic use of the `MailboxProcessor` class.  
  
 [!CODE [FsMailboxProcessor#2](../CodeSnippet/VS_Snippets_Fsharp/fsmailboxprocessor#2)]  
  
 **Sample Output**  
  
 **Press any key...**  
**Message count = 0. Waiting for next message.**  
**Message received. ID: 1 Contents: ABC**  
**Message count = 1. Waiting for next message.**  
**Message received. ID: 2 Contents: XYZ**  
**Message count = 2. Waiting for next message.**   
## Example  
 The following example shows how to use `MailboxProcessor` to create a simple agent that accepts various types of messages and returns appropriate replies. This server agent represents a market maker, which is a buying and selling agent on a stock exchange that sets bid and ask prices for assets. Clients can query for prices, or buy and sell shares.  
  
 [!CODE [FsMailboxProcessor#3](../CodeSnippet/VS_Snippets_Fsharp/fsmailboxprocessor#3)]  
  
 **Sample Output**  
  
 **Posting message for AAA**  
**Replying with Info for AAA**  
**Posting message for BBB**  
**Replying with Notification:**  
**Bought 100 units of BBB at price $20.100000. Total purchase $2010.000000.**  
**Marketmaker balance: $   2010.00**  
**Posting message for CCC**  
**Replying with Notification:**  
**Sold 100 units of CCC at price $30.000000. Total sale $3000.000000.**  
**Marketmaker balance: $   -990.00**  
**Posting message for WrongCode**  
**Posting message with large number of shares of AAA.**  
**Insufficient shares to fulfill order for 1000000000 units of AAA.**  
**Posting message with too large a monetary amount.**  
**Insufficient cash to fulfill order for 100000000 units of AAA.**  
**Press any key...**  
**Posting BUY CCC 1338.**  
**Replying with Notification:**  
**Bought 1338 units of CCC at price $30.150000. Total purchase $40340.700000.**  
**Marketmaker balance: $  39350.70**  
**Program+Snippet3+Reply+Notify**  
**Posting BUY BBB 1961.**  
**Replying with Notification:**  
**Bought 1961 units of BBB at price $20.100000. Total purchase $39416.100000.**  
**Marketmaker balance: $  78766.80**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)