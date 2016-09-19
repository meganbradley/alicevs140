---
title: "LanguagePrimitives.GenericEqualityWithComparer&lt;&#39;T&gt; Function (F#)"
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
  - LanguagePrimitives.GenericEqualityWithComparer<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 6002b544-660c-4000-818d-047d4304c3a7
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LanguagePrimitives.GenericEqualityWithComparer&lt;&#39;T&gt; Function (F#)
Compare two values for equality.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
GenericEqualityWithComparer : IEqualityComparer -> 'T -> 'T -> bool (requires equality)  
  
// Usage:  
GenericEqualityWithComparer comp e1 e2  
```  
  
#### Parameters  
 `comp`  
 Type: <xref:System.Collections.IEqualityComparer?qualifyHint=False>  
  
 The comparer object.  
  
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