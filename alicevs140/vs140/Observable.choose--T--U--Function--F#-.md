---
title: "Observable.choose&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Observable.choose<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 75191474-af8a-4eb8-bc39-34f0e55a4368
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Observable.choose&lt;&#39;T,&#39;U&gt; Function (F#)
Returns an observable which chooses a projection of observations from the source using the given function. The returned object will trigger observations for which the splitter returns a `Some` value. The returned object also propagates all errors arising from the source and completes when the source completes.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.Observable  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Observable.choose : ('T -> 'U option) -> IObservable<'T> -> IObservable<'U>  
  
// Usage:  
Observable.choose chooser source  
```  
  
#### Parameters  
 `chooser`  
 Type: `'T -> 'U`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The function that returns `Some` for observations to be propagated and None for observations to ignore.  
  
 `source`  
 Type: [IObservable](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)`<'T>`  
  
 The input Observable.  
  
## Return Value  
 An Observable that only propagates some of the observations from the source.  
  
## Remarks  
 This function is named `Choose` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Observable Module (F#)](../vs140/Control.Observable-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)