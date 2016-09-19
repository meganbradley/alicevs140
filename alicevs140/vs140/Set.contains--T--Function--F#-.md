---
title: "Set.contains&lt;&#39;T&gt; Function (F#)"
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
  - Set.contains<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7d616d1e-bca9-463e-b11e-88b5dc8b930b
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.contains&lt;&#39;T&gt; Function (F#)
Evaluates to `true` if the given element is in the given set.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Set  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.contains : 'T -> Set<'T> -> bool (requires comparison)  
  
// Usage:  
Set.contains element set  
```  
  
#### Parameters  
 `element`  
 Type: `'T`  
  
 The element to test.  
  
 `set`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The input set.  
  
## Return Value  
 True if `element` is in `set`.  
  
## Remarks  
 This function is named `Contains` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)