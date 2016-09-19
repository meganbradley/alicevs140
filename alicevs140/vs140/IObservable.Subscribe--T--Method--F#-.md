---
title: "IObservable.Subscribe&lt;&#39;T&gt; Method (F#)"
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
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e9c09e03-b1f9-4975-b992-1f222e8298ae
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IObservable.Subscribe&lt;&#39;T&gt; Method (F#)
Subscribe an observer to the source of results  
  
 **Namespace/Module Path**: System  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
abstract this.Subscribe : IObserver<'T> -> IDisposable  
  
// Usage:  
iObservable.Subscribe (observer)  
```  
  
#### Parameters  
 `observer`  
 Type: [IObserver](../Topic/System.IObserver%3C'T%3E%20Interface%20\(F%23\).md)`<'T>`  
  
 The observer to be added to those that are notified.  
  
## Return Value  
 An IDisposable to allow for unsubscription.  
  
## Remarks  
 This API is provided for use only with the F# Core Library Versions that targets .NET Framework 2.0. If you are using .NET Framework 4, use the .NET Framework 4 API with the same name, <xref:System.IObservable`1.Subscribe?qualifyHint=False>.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0  
  
## See Also  
 [System.IObservable<'T> Interface (F#)](../Topic/System.IObservable%3C'T%3E%20Interface%20\(F%23\).md)   
 [System Namespace (F#)](../Topic/System%20Namespace%20\(F%23\).md)