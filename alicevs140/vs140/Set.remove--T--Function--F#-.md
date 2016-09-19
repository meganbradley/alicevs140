---
title: "Set.remove&lt;&#39;T&gt; Function (F#)"
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
  - Set.remove<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 812a6d19-c1f0-4c57-9cbe-15d141d64ddb
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.remove&lt;&#39;T&gt; Function (F#)
Returns a new set with the given element removed. No exception is raised if the set does not contain the given element.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Set  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.remove : 'T -> Set<'T> -> Set<'T> (requires comparison)  
  
// Usage:  
Set.remove value set  
```  
  
#### Parameters  
 `value`  
 Type: `'T`  
  
 The element to remove.  
  
 `set`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The input set.  
  
## Return Value  
 The input set with `value` removed.  
  
## Remarks  
 This function is named `Remove` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)