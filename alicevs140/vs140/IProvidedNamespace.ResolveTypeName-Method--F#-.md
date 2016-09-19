---
title: "IProvidedNamespace.ResolveTypeName Method (F#)"
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
ms.assetid: a2ae63b1-9acf-45a1-91b8-132e5759aa2e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IProvidedNamespace.ResolveTypeName Method (F#)
Compilers call this method to query a type provider for a type name.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.CompilerServices  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
abstract this.ResolveTypeName : string -> Type  
  
// Usage:  
iProvidedNamespace.ResolveTypeName (typeName)  
```  
  
#### Parameters  
 `typeName`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
## Return Value  
  
## Remarks  
 Resolver should return a type called `name` in namespace `NamespaceName` or `null` if the type is unknown.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [CompilerServices.IProvidedNamespace Interface (F#)](../vs140/CompilerServices.IProvidedNamespace-Interface--F#-.md)