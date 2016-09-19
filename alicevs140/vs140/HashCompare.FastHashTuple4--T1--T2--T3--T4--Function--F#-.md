---
title: "HashCompare.FastHashTuple4&lt;&#39;T1,&#39;T2,&#39;T3,&#39;T4&gt; Function (F#)"
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
ms.assetid: 9aa3ad55-c232-4639-8f88-bc2d01ab4c9c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HashCompare.FastHashTuple4&lt;&#39;T1,&#39;T2,&#39;T3,&#39;T4&gt; Function (F#)
A primitive entry point used by the F# compiler for optimization purposes.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives.HashCompare  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
FastHashTuple4 : IEqualityComparer -> 'T1 * 'T2 * 'T3 * 'T4 -> int  
  
// Usage:  
FastHashTuple4 comparer tuple  
```  
  
#### Parameters  
 `comparer`  
 Type: <xref:System.Collections.IEqualityComparer?qualifyHint=False>  
  
 The comparer object.  
  
 `tuple`  
 Type: `'T1 * 'T2 * 'T3 * 'T4`  
  
 A tuple of four elements.  
  
## Return Value  
 The computed hash.  
  
## Remarks  
 This function is for use by compiled F# code and should not be used directly.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [LanguagePrimitives.HashCompare Module (F#)](../vs140/LanguagePrimitives.HashCompare-Module--F#-.md)   
 [Microsoft.FSharp.Core.LanguagePrimitives Namespace (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)