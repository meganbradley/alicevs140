---
title: "Observable.merge&lt;&#39;T&gt; Function (F#)"
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
  - Observable.merge<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 33e40753-6895-41a8-acd5-85fcb4eb7524
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Observable.merge&lt;&#39;T&gt; Function (F#)
Returns an observable for the merged observations from the sources. The returned object propagates success and error values arising from either source and completes when both the sources have completed.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.Observable  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Observable.merge : IObservable<'T> -> IObservable<'T> -> IObservable<'T>  
  
// Usage:  
Observable.merge source1 source2  
```  
  
#### Parameters  
 `source1`  
 Type: [IObservable](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)`<'T>`  
  
 The first Observable.  
  
 `source2`  
 Type: [IObservable](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)`<'T>`  
  
 The second Observable.  
  
## Return Value  
 An Observable that propagates information from both sources.  
  
## Remarks  
 For each observer, the registered intermediate observing object is not thread safe. That is, observations arising from the sources must not be triggered concurrently on different threads.  
  
 This function is named `Merge` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Observable Module (F#)](../vs140/Control.Observable-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)