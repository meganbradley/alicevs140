---
title: "LanguagePrimitives.GenericComparisonWithComparer&lt;&#39;T&gt; Function (F#)"
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
  - LanguagePrimitives.GenericComparisonWithComparer<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7e4ae86f-4f64-4b3d-97b7-53ce2ac6c572
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LanguagePrimitives.GenericComparisonWithComparer&lt;&#39;T&gt; Function (F#)
Compare two values. May be called as a recursive case from an implementation of <xref:System.IComparable`1?qualifyHint=False> to ensure consistent NaN comparison semantics.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
GenericComparisonWithComparer : IComparer -> 'T -> 'T -> int (requires comparison)  
  
// Usage:  
GenericComparisonWithComparer comp e1 e2  
```  
  
#### Parameters  
 `comp`  
 Type: <xref:System.Collections.IComparer?qualifyHint=False>  
  
 The function to compare the values.  
  
 `e1`  
 Type: `'T`  
  
 The first value.  
  
 `e2`  
 Type: `'T`  
  
 The second value.  
  
## Return Value  
 The result of the comparison.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.LanguagePrimitives Module (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)