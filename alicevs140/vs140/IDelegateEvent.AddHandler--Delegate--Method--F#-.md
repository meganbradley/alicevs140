---
title: "IDelegateEvent.AddHandler&lt;&#39;Delegate&gt; Method (F#)"
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
  - IDelegateEvent.AddHandler<'Delegate>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 15ff9fc8-43e6-456f-b0f7-5cd104bb6d9a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDelegateEvent.AddHandler&lt;&#39;Delegate&gt; Method (F#)
Connect a handler delegate object to the event. A handler can be later removed using [RemoveHandler](../vs140/IDelegateEvent.RemoveHandler--Delegate--Method--F#-.md). The listener will be invoked when the event is fired.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
abstract this.AddHandler : 'Delegate -> unit  
  
// Usage:  
iDelegateEvent.AddHandler (handler)  
```  
  
#### Parameters  
 `handler`  
 Type: `'Delegate`  
  
 A delegate to be invoked when the event is fired.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.IDelegateEvent<'Delegate> Interface (F#)](../vs140/Control.IDelegateEvent--Delegate--Interface--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)