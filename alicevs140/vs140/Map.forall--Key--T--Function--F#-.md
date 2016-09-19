---
title: "Map.forall&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.forall<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 184ced53-597e-47e1-90d0-47926a81bf92
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.forall&lt;&#39;Key,&#39;T&gt; Function (F#)
Returns `true` if the given predicate returns `true` for all of the bindings in the map.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Map  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.forall : ('Key -> 'T -> bool) -> Map<'Key,'T> -> bool (requires comparison)  
  
// Usage:  
Map.forall predicate table  
```  
  
#### Parameters  
 `predicate`  
 Type: `'Key -> 'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Return Value  
 `true` if the predicate evaluates to `true` for all of the bindings in the map.  
  
## Remarks  
 This function is named `ForAll` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Map.forall`.  
  
 [!CODE [FsMaps#11](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#11)]  
  
 **Output**  
  
 **true false**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)