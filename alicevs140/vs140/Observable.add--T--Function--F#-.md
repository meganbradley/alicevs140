---
title: "Observable.add&lt;&#39;T&gt; Function (F#)"
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
  - Observable.add<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f4723e85-4fd0-41e5-b31a-a6f2cf07c43a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Observable.add&lt;&#39;T&gt; Function (F#)
Creates an observer which permanently subscribes to the given observable and which calls the given function for each observation.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.Observable  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Observable.add : ('T -> unit) -> IObservable<'T> -> unit  
  
// Usage:  
Observable.add callback source  
```  
  
#### Parameters  
 `callback`  
 Type: `'T ->`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 The function to be called on each observation.  
  
 `source`  
 Type: [IObservable](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)`<'T>`  
  
 The input Observable.  
  
## Remarks  
 This function is named `Add` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Observable Module (F#)](../vs140/Control.Observable-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)