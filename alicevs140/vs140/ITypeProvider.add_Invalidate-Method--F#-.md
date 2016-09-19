---
title: "ITypeProvider.add_Invalidate Method (F#)"
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
ms.assetid: 4d396b82-cbdb-4334-85c7-47b83d4ec16e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITypeProvider.add_Invalidate Method (F#)
Add an event handler to the [Invalidate](../vs140/ITypeProvider.Invalidate-Event--F#-.md) event.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.CompilerServices  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
abstract this.add_Invalidate : EventHandler -> unit  
  
// Usage:  
iTypeProvider.add_Invalidate ()  
```  
  
#### Parameters  
 `handler`  
 Type: <xref:System.EventHandler?qualifyHint=False>  
  
 The event handler to add.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [CompilerServices.ITypeProvider Interface (F#)](../Topic/CompilerServices.ITypeProvider%20Interface%20\(F%23\).md)   
 [Microsoft.FSharp.Core.CompilerServices Namespace (F#)](../vs140/Microsoft.FSharp.Core.CompilerServices-Namespace--F#-.md)