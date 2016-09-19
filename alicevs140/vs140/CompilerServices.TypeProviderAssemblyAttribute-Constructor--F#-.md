---
title: "CompilerServices.TypeProviderAssemblyAttribute Constructor (F#)"
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
ms.assetid: ae7daf6f-4c71-4032-9046-ffceeb8f408a
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CompilerServices.TypeProviderAssemblyAttribute Constructor (F#)
Creates an instance of the attribute.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.CompilerServices  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signatures:  
new TypeProviderAssemblyAttribute : string -> TypeProviderAssemblyAttribute  
new TypeProviderAssemblyAttribute : unit -> TypeProviderAssemblyAttribute  
  
// Usage:  
new TypeProviderAssemblyAttribute (assemblyName)  
new TypeProviderAssemblyAttribute ()  
```  
  
#### Parameters  
 `assemblyName`  
 Type:  [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The name of the design-time assembly for this type provider.  
  
## Return Value  
 A new instance of `TypeProviderAssemblyAttribute`.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2,  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [CompilerServices.TypeProviderAssemblyAttribute Class (F#)](../vs140/CompilerServices.TypeProviderAssemblyAttribute-Class--F#-.md)   
 [Microsoft.FSharp.Core.CompilerServices Namespace (F#)](../vs140/Microsoft.FSharp.Core.CompilerServices-Namespace--F#-.md)