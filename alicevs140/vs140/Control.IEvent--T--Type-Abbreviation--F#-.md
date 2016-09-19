---
title: "Control.IEvent&lt;&#39;T&gt; Type Abbreviation (F#)"
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
  - Control.IEvent<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7976554f-9aa8-451f-a69d-d4670c064432
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control.IEvent&lt;&#39;T&gt; Type Abbreviation (F#)
Represents first-class listening points, that is, objects that permit you to register a callback activated when the event is triggered).  
  
 This type is an abbreviation for [Control.IEvent<Handler<'T>,'Args>](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type IEvent<'T> = IEvent<'Delegate,'Args (requires delegate)>  
```  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)   
 [Control.IEvent<'Delegate,'Args>](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)