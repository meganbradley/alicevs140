---
title: "Handler.Invoke&lt;&#39;T&gt; Method (F#)"
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
  - Handler.Invoke<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 0f42e201-6463-4d42-a659-44f29138b4cd
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Handler.Invoke&lt;&#39;T&gt; Method (F#)
Calls the function or functions associated with the event handler.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
abstract this.Invoke : obj * 'T -> unit  
  
// Usage:  
handler.Invoke (sender, args)  
```  
  
#### Parameters  
 `sender`  
 Type: [obj](../Topic/Core.obj%20Type%20Abbreviation%20\(F%23\).md)  
  
 The object that fired the event.  
  
 `args`  
 Type: `'T`  
  
 The event arguments.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Handler<'T> Class (F#)](../vs140/Control.Handler--T--Class--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)