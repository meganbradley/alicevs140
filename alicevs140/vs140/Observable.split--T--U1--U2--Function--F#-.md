---
title: "Observable.split&lt;&#39;T,&#39;U1,&#39;U2&gt; Function (F#)"
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
  - Observable.split<'T,'U1,'U2>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a628f66b-8712-4a5d-b9fc-ba2f323cb333
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Observable.split&lt;&#39;T,&#39;U1,&#39;U2&gt; Function (F#)
Returns two observables which split the observations of the source by the given function. The first will trigger observations for which the splitter returns `Choice1Of2`. The second will trigger observations `y` for which the splitter returns `Choice2Of2`. The splitter is executed once for each subscribed observer. Both also propagate error observations arising from the source and each completes when the source completes.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control.Observable  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Observable.split : ('T -> Choice<'U1,'U2>) -> IObservable<'T> -> IObservable<'U1> * IObservable<'U2>  
  
// Usage:  
Observable.split splitter source  
```  
  
#### Parameters  
 `splitter`  
 Type: `'T ->` [Choice](../vs140/Core.Choice--T1--T2--Union--F#-.md)`<'U1,'U2>`  
  
 The function that takes an observation and transforms it into one of the two output [Choice](../vs140/Core.Choice--T1--T2--Union--F#-.md) types.  
  
 `source`  
 Type: [IObservable](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)`<'T>`  
  
 The input Observable.  
  
## Return Value  
 A tuple of Observables. The first triggers when `splitter` returns `Choice1of2` and the second triggers when `splitter` returns `Choice2of2`.  
  
## Remarks  
 This function is named `Split` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Observable Module (F#)](../vs140/Control.Observable-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)