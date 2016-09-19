---
title: "Operators.typedefof&lt;&#39;T&gt; Type Function (F#)"
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
apiname: 
  - Operators.typedefof<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 3d215077-adc1-4261-a74f-04b22a09916e
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.typedefof&lt;&#39;T&gt; Type Function (F#)
Generate a <xref:System.Type?qualifyHint=False> representation for a type definition. If the input type is a generic type instantiation then return the generic type definition associated with all such instantiations.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
typedefof<'T> :  Type  
  
// Usage:  
typedefof  
```  
  
## Return Value  
 A <xref:System.Type?qualifyHint=False> object representing the type of the expression, or generic type, if applicable.  
  
## Remarks  
 This function is named `TypeDefOf` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)