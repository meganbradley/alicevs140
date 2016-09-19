---
title: "Observable.subscribe&lt;&#39;T&gt; Function (F#)"
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
  - Observable.subscribe<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 19e66519-0b77-4396-8159-67ec47be0a63
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Observable.subscribe&lt;&#39;T&gt; Function (F#)
Creates an observer which subscribes to the given observable and which calls the given function for each observation.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control.Observable  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Observable.subscribe : ('T -> unit) -> IObservable<'T> -> IDisposable  
  
// Usage:  
Observable.subscribe callback source  
```  
  
#### Parameters  
 `callback`  
 Type: `'T ->`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 The function to be called on each observation.  
  
 `source`  
 Type: [IObservable](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)`<'T>`  
  
 The input Observable.  
  
## Return Value  
 An object that will remove the callback if disposed.  
  
## Remarks  
 This function is named `Subscribe` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Observable Module (F#)](../vs140/Control.Observable-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)