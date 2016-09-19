---
title: "Observable.filter&lt;&#39;T&gt; Function (F#)"
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
  - Observable.filter<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c7957b74-9d92-4a5d-9f0a-43b51179e6c8
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Observable.filter&lt;&#39;T&gt; Function (F#)
Returns an observable which filters the observations of the source by the given function. The observable will see only those observations for which the predicate returns true. The predicate is executed once for each subscribed observer. The returned object also propagates error observations arising from the source and completes when the source completes.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.Observable  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Observable.filter : ('T -> bool) -> IObservable<'T> -> IObservable<'T>  
  
// Usage:  
Observable.filter predicate source  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to apply to observations to determine if it should be kept.  
  
 `source`  
 Type: [IObservable](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)`<'T>`  
  
 The input Observable.  
  
## Return Value  
 An Observable that filters observations based on `filter`.  
  
## Remarks  
 This function is named `Filter` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Observable Module (F#)](../vs140/Control.Observable-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)