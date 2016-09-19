---
title: "Event.filter&lt;&#39;T,&#39;Del&gt; Function (F#)"
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
ms.assetid: 8469b9e3-5513-4059-b216-2011a631022a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event.filter&lt;&#39;T,&#39;Del&gt; Function (F#)
Returns a new event that listens to the original event and triggers the resulting event only when the argument to the event passes the given function.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.Event  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Event.filter : ('T -> bool) -> IEvent<'Del,'T> -> IEvent<'T> (requires delegate)  
  
// Usage:  
Event.filter predicate sourceEvent  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to determine which triggers from the event to propagate.  
  
 `sourceEvent`  
 Type: [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)`<'Del,'T>`  
  
 The input event.  
  
## Return Value  
 An event that only passes values that pass the predicate.  
  
## Remarks  
 This function is named `Filter` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example shows how to use the `Event.filter` function. In this example, mouse events are passed on only when the mouse pointer is in a certain region.  
  
 [!CODE [FsEvents#3](../CodeSnippet/VS_Snippets_Fsharp/fsevents#3)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Event Module (F#)](../vs140/Control.Event-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)