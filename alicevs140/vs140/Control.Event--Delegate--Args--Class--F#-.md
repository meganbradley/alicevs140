---
title: "Control.Event&lt;&#39;Delegate,&#39;Args&gt; Class (F#)"
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
  - Control.FSharpEvent<'Delegate,'Args>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 114c0f1a-1c34-46d4-a93a-b629e6ddd13c
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control.Event&lt;&#39;Delegate,&#39;Args&gt; Class (F#)
Event implementations for a delegate types following the standard .NET Framework convention of a first `sender` argument.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type Event<'Delegate,'Args (requires delegate)> =  
 class  
  new Event : unit -> Event<'Delegate,'Args>  
  member this.Trigger : obj * 'Args -> unit  
  member this.Publish :  IEvent<'Delegate,'Args>  
 end  
```  
  
## Remarks  
 This type is named `FSharpEvent` in compiled assemblies. If you are accessing the type from a language other than F#, or through reflection, use this name.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Control.Event--Delegate--Args--Constructor--F#-.md)|Creates an event object suitable for delegate types following the standard .NET Framework convention of a first 'sender' argument.|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Publish](../vs140/Event.Publish--Delegate--Args--Property--F#-.md)|Publishes the event as a first class event value.|  
|[Trigger](../vs140/Event.Trigger--Delegate--Args--Method--F#-.md)|Triggers the event using the given sender object and parameters. The sender object may be `null`.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)