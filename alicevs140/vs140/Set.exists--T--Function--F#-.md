---
title: "Set.exists&lt;&#39;T&gt; Function (F#)"
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
  - Set.exists<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 55bf43f8-e5f2-4e3d-900a-e4d7ca983541
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.exists&lt;&#39;T&gt; Function (F#)
Tests if any element of the collection satisfies the given predicate. If the input function is `predicate` and the elements are `i0...iN`, then this function computes `p i0 or ... or p iN`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Set  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.exists : ('T -> bool) -> Set<'T> -> bool (requires comparison)  
  
// Usage:  
Set.exists predicate set  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test set elements.  
  
 `set`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The input set.  
  
## Return Value  
 True if any element of `set` satisfies `predicate`.  
  
## Remarks  
 This function is named `Exists` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)