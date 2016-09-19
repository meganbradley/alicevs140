---
title: "Event.merge&lt;&#39;Del1,&#39;T,&#39;Del2&gt; Function (F#)"
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
ms.assetid: 4eb364ff-9a40-41cf-b62e-64a80576fdc6
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event.merge&lt;&#39;Del1,&#39;T,&#39;Del2&gt; Function (F#)
Fires the output event when either of the input events fire.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.Event  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Event.merge : IEvent<'Del1,'T> -> IEvent<'Del2,'T> -> IEvent<'T> (requires delegate and delegate)  
  
// Usage:  
Event.merge event1 event2  
```  
  
#### Parameters  
 `event1`  
 Type: [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)`<'Del1,'T>`  
  
 The first input event.  
  
 `event2`  
 Type: [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)`<'Del2,'T>`  
  
 The second input event.  
  
## Return Value  
 An event that fires when either of the input events fire.  
  
## Remarks  
 This function is named `Merge` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example shows how to use the `Event.merge` function.  
  
 [!CODE [FsEvents#5](../CodeSnippet/VS_Snippets_Fsharp/fsevents#5)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Event Module (F#)](../vs140/Control.Event-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)