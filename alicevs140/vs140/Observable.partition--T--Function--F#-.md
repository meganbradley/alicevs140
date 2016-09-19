---
title: "Observable.partition&lt;&#39;T&gt; Function (F#)"
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
  - Observable.partition<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 31619722-11a8-498c-88e4-8be7591a2160
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Observable.partition&lt;&#39;T&gt; Function (F#)
Returns two observables which partition the observations of the source by the given function. The first will trigger observations for those values for which the predicate returns true. The second will trigger observations for those values where the predicate returns false. The predicate is executed once for each subscribed observer. Both also propagate all error observations arising from the source and each completes when the source completes.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.Observable  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Observable.partition : ('T -> bool) -> IObservable<'T> -> IObservable<'T> * IObservable<'T>  
  
// Usage:  
Observable.partition predicate source  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to determine which output Observable will trigger a particular observation.  
  
 `source`  
 Type: [IObservable](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)`<'T>`  
  
 The input Observable.  
  
## Return Value  
 A tuple of observables. The first triggers when the predicate returns `true`, and the second triggers when the predicate returns `false`.  
  
## Remarks  
 This function is named `Partition` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Observable Module (F#)](../vs140/Control.Observable-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)