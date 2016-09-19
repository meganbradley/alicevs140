---
title: "Event.pairwise&lt;&#39;Del,&#39;T&gt; Function (F#)"
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
ms.assetid: ee175ad7-653e-415a-8929-decbd5b4e1c7
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event.pairwise&lt;&#39;Del,&#39;T&gt; Function (F#)
Returns a new event that triggers on the second and subsequent triggerings of the input event. The Nth triggering of the input event passes the arguments from the N-1th and Nth triggering as a pair. The argument passed to the N-1th triggering is held in hidden internal state until the Nth triggering occurs.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control.Event  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Event.pairwise : IEvent<'Del,'T> -> IEvent<'T * 'T> (requires delegate)  
  
// Usage:  
Event.pairwise sourceEvent  
```  
  
#### Parameters  
 `sourceEvent`  
 Type: [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)`<'Del,'T>`  
  
 The input event.  
  
## Return Value  
 An event that triggers on pairs of consecutive values passed from the source event.  
  
## Remarks  
 This function is named `Pairwise` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example shows how to use the `Event.pairwise` function. In this example, the function makes data available from more than one `MouseMove` event, and the data is used to draw a line between consecutive mouse positions.  
  
 [!CODE [FsEvents#6](../CodeSnippet/VS_Snippets_Fsharp/fsevents#6)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Event Module (F#)](../vs140/Control.Event-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)