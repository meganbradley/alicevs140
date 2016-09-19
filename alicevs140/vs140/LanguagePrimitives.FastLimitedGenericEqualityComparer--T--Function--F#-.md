---
title: "LanguagePrimitives.FastLimitedGenericEqualityComparer&lt;&#39;T&gt; Function (F#)"
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
  - LanguagePrimitives.FastLimitedGenericEqualityComparer<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8d6de104-6a02-4805-bb97-d2670e5555a5
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LanguagePrimitives.FastLimitedGenericEqualityComparer&lt;&#39;T&gt; Function (F#)
Make an F# hash/equality object for the given type using node-limited hashing when hashing F# records, lists and union types.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
FastLimitedGenericEqualityComparer : int -> IEqualityComparer<'T> (requires equality)  
  
// Usage:  
FastLimitedGenericEqualityComparer limit  
```  
  
#### Parameters  
 `limit`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The input limit on the number of nodes.  
  
## Return Value  
 The hash/equality object as a <xref:System.Collections.Generic.IEqualityComparer`1?qualifyHint=False>.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.LanguagePrimitives Module (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)