---
title: "ITypeProvider.GetNamespaces Method (F#)"
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
ms.assetid: eac5d16b-5eb7-4911-b383-20862217ae02
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITypeProvider.GetNamespaces Method (F#)
Namespace names into which this type provider injects types.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.CompilerServices  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
abstract this.GetNamespaces : unit -> IProvidedNamespace []  
  
// Usage:  
iTypeProvider.GetNamespaces ()  
```  
  
## Return Value  
 An array of provided namespaces that contain provided types.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0Supported in: 4.0, Portable  
  
## See Also  
 [CompilerServices.ITypeProvider Interface (F#)](../Topic/CompilerServices.ITypeProvider%20Interface%20\(F%23\).md)   
 [Microsoft.FSharp.Core.CompilerServices Namespace (F#)](../vs140/Microsoft.FSharp.Core.CompilerServices-Namespace--F#-.md)