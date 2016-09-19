---
title: "Set.isProperSuperset&lt;&#39;T&gt; Function (F#)"
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
  - Set.isProperSuperset<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 64bb2c29-59db-4d2c-9a54-7a0440b4e37f
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.isProperSuperset&lt;&#39;T&gt; Function (F#)
Evaluates to `true` if all elements of the second set are in the first, and at least one element of the first is not in the second.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Set  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.isProperSuperset : Set<'T> -> Set<'T> -> bool (requires comparison)  
  
// Usage:  
Set.isProperSuperset set1 set2  
```  
  
#### Parameters  
 `set1`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The potential superset.  
  
 `set2`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The set to test against.  
  
## Return Value  
 True if `set1` is a proper superset of `set2`.  
  
## Remarks  
 This function is named `IsProperSuperset` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of the `Set.isProperSuperset` function.  
  
 [!CODE [FsSets#9](../CodeSnippet/VS_Snippets_Fsharp/fssets#9)]  
  
 **Output**  
  
 **set [1; 2; 3; 4; 5; 6; 7; 8; 9] is a proper superset of set [1; 2; 3; 4; 5; 6]: true**  
**set [1; 2; 3; 4; 5; 6] is a proper superset of set [1; 2; 3; 4; 5; 6]: false**  
**set [5; 6; 7; 8; 9; 10] is a proper superset of set [1; 2; 3; 4; 5; 6]: false**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)