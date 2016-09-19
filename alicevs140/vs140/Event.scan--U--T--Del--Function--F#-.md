---
title: "Event.scan&lt;&#39;U,&#39;T,&#39;Del&gt; Function (F#)"
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
ms.assetid: 17ab718c-2ed5-4e1a-8b93-49007fed9cb5
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event.scan&lt;&#39;U,&#39;T,&#39;Del&gt; Function (F#)
Returns a new event that consists of the results of applying the given accumulating function to successive values triggered on the input event.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.Event  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Event.scan : ('U -> 'T -> 'U) -> 'U -> IEvent<'Del,'T> -> IEvent<'U> (requires delegate)  
  
// Usage:  
Event.scan collector state sourceEvent  
```  
  
#### Parameters  
 `collector`  
 Type: `'U -> 'T -> 'U`  
  
 The function to update the state with each event value.  
  
 `state`  
 Type: `'U`  
  
 The initial state.  
  
 `sourceEvent`  
 Type: [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)`<'Del,'T>`  
  
 The input event.  
  
## Return Value  
 An event that fires on the updated state values.  
  
## Remarks  
 An item of internal state records the current value of the state parameter. The internal state is not locked during the execution of the accumulation function, so care should be taken that the input [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md) is not triggered by multiple threads simultaneously.  
  
 This function is named `Scan` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example shows how to use the `Event.scan` function. This code implements a simple click counter. Every time the user clicks on the form, the state increments by 1 and the form's text is changed to display the new state.  
  
 [!CODE [FsEvents#8](../CodeSnippet/VS_Snippets_Fsharp/fsevents#8)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Event Module (F#)](../vs140/Control.Event-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)