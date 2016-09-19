---
title: "Map.pick&lt;&#39;Key,&#39;T,&#39;U&gt; Function (F#)"
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
  - Map.pick<'Key,'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a7868ddd-13aa-443d-9ac0-e16205b77681
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.pick&lt;&#39;Key,&#39;T,&#39;U&gt; Function (F#)
Searches the map looking for the first element where the given function returns a `Some` value  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Map  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.pick : ('Key -> 'T -> 'U option) -> Map<'Key,'T> -> 'U (requires comparison)  
  
// Usage:  
Map.pick chooser table  
```  
  
#### Parameters  
 `chooser`  
 Type: `'Key -> 'T -> 'U`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The function to generate options from the key/value pairs.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Return Value  
 The first result.  
  
## Remarks  
 This function is named `Pick` in compiled assembly. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Map.pick`.  
  
 [!CODE [FsMaps#14](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#14)]  
  
 **Output**  
  
 **Result where key and value are the same: 50**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)