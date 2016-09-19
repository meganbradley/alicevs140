---
title: "Event.split&lt;&#39;T,&#39;U1,&#39;U2,&#39;Del&gt; Function (F#)"
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
ms.assetid: 90f126ec-3726-4ea5-8626-0463be8d9e7a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event.split&lt;&#39;T,&#39;U1,&#39;U2,&#39;Del&gt; Function (F#)
Returns a new event that listens to the original event and triggers the first resulting event if the application of the function to the event arguments returned a `Choice1Of2`, and the second event if it returns a `Choice2Of2`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.Event  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Event.split : ('T -> Choice<'U1,'U2>) -> IEvent<'Del,'T> -> IEvent<'U1> * IEvent<'U2> (requires delegate)  
  
// Usage:  
Event.split splitter sourceEvent  
```  
  
#### Parameters  
 `splitter`  
 Type: `'T ->`[Choice](../vs140/Core.Choice--T1--T2--Union--F#-.md)`<'U1,'U2>`  
  
 A function, typically an active pattern recognizer, that transforms event values into one of two types.  
  
 `sourceEvent`  
 Type: [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)`<'Del,'T>`  
  
 The input event.  
  
## Return Value  
 A tuple of events. The first fires whenever `splitter` evaluates to Choice1of1 and the second fires whenever `splitter` evaluates to Choice2of2.  
  
## Remarks  
 This function is named `Split` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use the `Event.split` function to implement the ability to move a control on a form. The `splitter` function is the active pattern recognizer `(|Down|Up|)`, which represents the state of the mouse buttons. If a user presses the mouse button while moving the mouse when it is over the button, the button moves. There is also code that sometimes changes the color of the button while it is moving, depending on which mouse button is used. This test uses a different color for each mouse button. The other event path, which is used when the mouse button is not down, restores the original color of the button after the button is released.  
  
 [!CODE [FsEvents#9](../CodeSnippet/VS_Snippets_Fsharp/fsevents#9)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Event Module (F#)](../vs140/Control.Event-Module--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)