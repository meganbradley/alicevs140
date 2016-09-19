---
title: "MailboxProcessor.remove_Error&lt;&#39;Msg&gt; Method (F#)"
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
  - MailboxProcessor.remove_Error<'Msg>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: bfbc587c-9317-4094-8091-8519d8a47a37
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MailboxProcessor.remove_Error&lt;&#39;Msg&gt; Method (F#)
Occurs when the execution of the agent results in an exception.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.remove_Error : Handler<Exception> -> unit  
  
// Usage:  
mailboxProcessor.remove_Error ()  
```  
  
#### Parameters  
 Type: [Handler](../vs140/Control.Handler--T--Class--F#-.md)`<`<xref:System.Exception?qualifyHint=False>`>`  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.MailboxProcessor<'Msg> Class (F#)](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)