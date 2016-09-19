---
title: "Set.partition&lt;&#39;T&gt; Function (F#)"
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
  - Set.partition<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e5406822-361f-441b-ab6f-f22326b66320
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.partition&lt;&#39;T&gt; Function (F#)
Splits the set into two sets containing the elements for which the given predicate returns `true` and `false` respectively.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Set  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.partition : ('T -> bool) -> Set<'T> -> Set<'T> * Set<'T> (requires comparison)  
  
// Usage:  
Set.partition predicate set  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->` [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test set elements.  
  
 `set`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The input set.  
  
## Return Value  
 A pair of sets. The first contains the elements for which `predicate` returns `true` and the second contains the elements for which `predicate` returns `false`.  
  
## Remarks  
 This function is named `Partition` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)