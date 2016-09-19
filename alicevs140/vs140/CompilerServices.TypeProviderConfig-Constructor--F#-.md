---
title: "CompilerServices.TypeProviderConfig Constructor (F#)"
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
ms.assetid: a58edc91-0eae-49b8-9331-81115832f7af
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CompilerServices.TypeProviderConfig Constructor (F#)
Constructor for TypeProviderConfig.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.CompilerServices  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
new TypeProviderConfig : string * string * string [] * string -> TypeProviderConfig  
  
// Usage:  
new TypeProviderConfig (resolutionFolder, runtimeAssembly, referencedAssemblies, temporaryFolder)  
```  
  
#### Parameters  
 `resolutionFolder`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The folder in which the resolution is occurring. Typically the project folder.  
  
 `runtimeAssembly`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 `referencedAssemblies`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 `temporaryFolder`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
## Return Value  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [CompilerServices.TypeProviderConfig Class (F#)](../Topic/CompilerServices.TypeProviderConfig%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Core.CompilerServices Namespace (F#)](../vs140/Microsoft.FSharp.Core.CompilerServices-Namespace--F#-.md)