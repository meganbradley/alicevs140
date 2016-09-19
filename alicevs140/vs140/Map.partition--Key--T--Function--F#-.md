---
title: "Map.partition&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.partition<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 97896a64-ef03-43d2-9000-51cad86c2200
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.partition&lt;&#39;Key,&#39;T&gt; Function (F#)
Creates two new maps, one containing the bindings for which the given predicate returns `true`, and the other the remaining bindings.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Map  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.partition : ('Key -> 'T -> bool) -> Map<'Key,'T> -> Map<'Key,'T> * Map<'Key,'T> (requires comparison)  
  
// Usage:  
Map.partition predicate table  
```  
  
#### Parameters  
 `predicate`  
 Type: `'Key -> 'T ->` [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Return Value  
 A pair of maps in which the first contains the elements for which the predicate returned `true` and the second containing the elements for which the predicated returned `false`.  
  
## Remarks  
 This function is named `Partition` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use **Map.partition**.  
  
 [!CODE [FsMaps#13](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#13)]  
  
 **Output**  
  
 **Evens: map [(2, 4); (4, 16); (6, 36); (8, 64); (10, 100)]**  
**Odds: map [(1, 1); (3, 9); (5, 25); (7, 49); (9, 81)]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)