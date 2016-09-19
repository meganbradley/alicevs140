---
title: "Set.toSeq&lt;&#39;T&gt; Function (F#)"
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
  - Set.to_seq<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 42338202-65da-4fc7-ad3f-101619e08f99
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.toSeq&lt;&#39;T&gt; Function (F#)
Returns an ordered view of the collection as an enumerable object.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Set  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.toSeq : Set<'T> -> seq<'T> (requires comparison)  
  
// Usage:  
Set.toSeq set  
```  
  
#### Parameters  
 `set`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The input set.  
  
## Return Value  
 An ordered sequence of the elements of `set`.  
  
## Remarks  
 This function is named `ToSeq` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)