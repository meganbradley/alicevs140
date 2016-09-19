---
title: "Control.IEvent&lt;&#39;Delegate,&#39;Args&gt; Interface (F#)"
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
  - Control.IEvent<'Delegate,'Args>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8dbca0df-f8a1-40bd-8d50-aa26f6a8b862
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control.IEvent&lt;&#39;Delegate,&#39;Args&gt; Interface (F#)
First class event values for CLI events conforming to CLI Framework standards.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type IEvent<'Delegate,'Args when 'Delegate : delegate<'Args,unit> and 'Delegate :> System.Delegate> =  
 interface  
  inherit IObservable<'Args>  
  inherit IDelegateEvent<'Delegate>  
 end  
```  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 <xref:System.IObservable`1?qualifyHint=False>   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)   
 [IDelegateEvent](../vs140/Control.IDelegateEvent--Delegate--Interface--F#-.md)   
 [System.IObservable<'T> Interface (F#)](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)