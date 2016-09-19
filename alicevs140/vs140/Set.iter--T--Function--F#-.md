---
title: "Set.iter&lt;&#39;T&gt; Function (F#)"
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
  - Set.iter<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 3f10b1f1-c1c9-4a86-af37-41e9c8dd8f54
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.iter&lt;&#39;T&gt; Function (F#)
Applies the given function to each element of the set, in order according to the comparison function.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Set  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.iter : ('T -> unit) -> Set<'T> -> unit (requires comparison)  
  
// Usage:  
Set.iter action set  
```  
  
#### Parameters  
 `action`  
 Type: `'T ->`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 The function to apply to each element.  
  
 `set`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The input set.  
  
## Remarks  
 This function is named `Iterate` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)