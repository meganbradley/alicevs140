---
title: "Unchecked.equals&lt;&#39;T&gt; Function (F#)"
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
  - Unchecked.equals<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 9374146b-4f23-4162-aca7-ddcf999abd8e
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Unchecked.equals&lt;&#39;T&gt; Function (F#)
Perform generic equality on two values where the type of the values is not statically required to satisfy the equality constraint.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.Unchecked  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
equals : 'T -> 'T -> bool  
  
// Usage:  
equals lhs rhs   
```  
  
#### Parameters  
 `lhs`  
 Type: `'T`  
  
 The first value to compare.  
  
 `rhs`  
 Type: `'T`  
  
 The second value to compare.  
  
## Return Value  
 The result of the comparison.  
  
## Remarks  
 This function is named `Equals` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Operators.Unchecked Module (F#)](../vs140/Operators.Unchecked-Module--F#-.md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)