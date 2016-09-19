---
title: "Control.Event&lt;&#39;T&gt; Class (F#)"
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
  - Control.FSharpEvent<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f3b47c8a-4ee5-4ce8-9a72-ad305a17c4b9
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control.Event&lt;&#39;T&gt; Class (F#)
Event implementations for the [IEvent](../vs140/Control.IEvent--T--Type-Abbreviation--F#-.md) type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type Event<'T> =  
 class  
  new Event : unit -> Event<'T>  
  member this.Trigger : 'T -> unit  
  member this.Publish :  IEvent<'T>  
 end  
```  
  
## Remarks  
 Functions that work with events are defined in the [Event module](../vs140/Control.Event-Module--F#-.md).  
  
 This type is named `FSharpEvent` in compiled assemblies. If you are accessing the type from a language other than F#, or through reflection, use this name.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Control.Event--T--Constructor--F#-.md)|Creates an observable object.|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Publish](../vs140/Event.Publish--T--Property--F#-.md)|Publishes an observation as a first class value.|  
|[Trigger](../vs140/Event.Trigger--T--Method--F#-.md)|Triggers an observation using the given parameters.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)   
 [IEvent<_>](../vs140/Control.IEvent--T--Type-Abbreviation--F#-.md)   
 [Control.IEvent<'Del,'Args>](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)