---
title: "IEventLoop.Invoke&lt;&#39;T&gt; Method (F#)"
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
ms.assetid: f9002b6e-d525-4abc-ad4b-0ff0888c16d6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IEventLoop.Invoke&lt;&#39;T&gt; Method (F#)
Request that the given operation be run synchronously on the event loop.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Compiler.Interactive  
  
 **Assembly:** FSharp.Compiler.Interactive.Settings (in FSharp.Compiler.Interactive.Settings.dll)  
  
## Syntax  
  
```  
// Signature:  
abstract this.Invoke : (unit -> 'T) -> 'T  
  
// Usage:  
iEventLoop.Invoke (func)  
```  
  
#### Parameters  
 `func`  
 Type: [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md) `-> 'T`  
  
 A function to run on the event loop.  
  
## Return Value  
  
## Remarks  
  
## Platforms  
 Windows 7, Windows Vista SP2, Windows XP SP3, Windows XP x64 SP2, Windows Server 2008 R2, Windows Server 2008 SP2, Windows Server 2003 SP2  
  
## Version Information  
 **F# Runtime**  
  
 Supported in: 2.0, 4  
  
 **Silverlight**  
  
 Supported in: 3  
  
## See Also  
 [Interactive.IEventLoop Interface (F#)](../vs140/Interactive.IEventLoop-Interface--F#-.md)   
 [Microsoft.FSharp.Compiler.Interactive Namespace (F#)](../vs140/Microsoft.FSharp.Compiler.Interactive-Namespace--F#-.md)