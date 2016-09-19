---
title: "Event.partition&lt;&#39;T,&#39;Del&gt; Function (F#)"
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
ms.assetid: 9854e530-5bd1-4705-bec6-688f53d7a952
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event.partition&lt;&#39;T,&#39;Del&gt; Function (F#)
Returns a new event that listens to the original event and triggers the first resulting event if the application of the predicate to the event arguments returned `true`, and the second event if it returned `false`.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control.Event  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Event.partition : ('T -> bool) -> IEvent<'Del,'T> -> IEvent<'T> * IEvent<'T> (requires delegate)  
  
// Usage:  
Event.partition predicate sourceEvent  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to determine which output event to trigger.  
  
 `sourceEvent`  
 Type: [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)`<'Del,'T>`  
  
 The input event.  
  
## Return Value  
 A tuple of events. The first is triggered when the predicate evaluates to `true` and the second when the predicate evaluates to `false`.  
  
## Remarks  
 This function is named `Partition` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use the `Event.partition` function to split an event into two events, each with its own event handling code.  
  
 [!CODE [FsEvents#7](../CodeSnippet/VS_Snippets_Fsharp/fsevents#7)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Event Module (F#)](../vs140/Control.Event-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)