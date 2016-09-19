---
title: "Set.map&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Set.map<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a71c114e-5143-49a0-9fc7-adf83612742a
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.map&lt;&#39;T,&#39;U&gt; Function (F#)
Returns a new collection containing the results of applying the given function to each element of the input set.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Set  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.map : ('T -> 'U) -> Set<'T> -> Set<'U> (requires comparison and comparison)  
  
// Usage:  
Set.map mapping set  
```  
  
#### Parameters  
 `mapping`  
 Type: `'T -> 'U`  
  
 The function to transform elements of the input set.  
  
 `set`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The input set.  
  
## Return Value  
 A set containing the transformed elements.  
  
## Remarks  
 This function is named [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md) in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)