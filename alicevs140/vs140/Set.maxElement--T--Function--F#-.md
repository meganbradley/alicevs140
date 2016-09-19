---
title: "Set.maxElement&lt;&#39;T&gt; Function (F#)"
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
  - Set.maxElement<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 95ff87fd-243e-41a4-b1f8-9d6d3a9c0ad6
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.maxElement&lt;&#39;T&gt; Function (F#)
Returns the highest element in the set according to the ordering being used for the set.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Set  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.maxElement : Set<'T> -> 'T (requires comparison)  
  
// Usage:  
Set.maxElement set  
```  
  
#### Parameters  
 `set`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The input set.  
  
## Return Value  
 The max value from the set.  
  
## Remarks  
 This function is named `MaxElement` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)