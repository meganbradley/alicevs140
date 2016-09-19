---
title: "ExtraTopLevelOperators.set&lt;&#39;T&gt; Function (F#)"
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
  - ExtraTopLevelOperators.set<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a4ec6cdd-9ae6-47e5-afa3-c6610a22931e
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ExtraTopLevelOperators.set&lt;&#39;T&gt; Function (F#)
Builds a set from a sequence of objects. The objects are indexed using generic comparison.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.ExtraTopLevelOperators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
set : seq<'T> -> Set<'T> (requires comparison)  
  
// Usage:  
set elements  
```  
  
#### Parameters  
 `elements`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
## Return Value  
 A [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md) object created from the given sequence.  
  
## Remarks  
 This function is named `CreateSet` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.ExtraTopLevelOperators Module (F#)](../Topic/Core.ExtraTopLevelOperators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)