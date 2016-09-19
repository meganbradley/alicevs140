---
title: "Map.map&lt;&#39;Key,&#39;T,&#39;U&gt; Function (F#)"
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
  - Map.map<'Key,'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c47bdb4a-af6b-4317-8687-02379b81d4c9
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.map&lt;&#39;Key,&#39;T,&#39;U&gt; Function (F#)
Creates a new collection whose elements are the results of applying the given function to each of the elements of the collection. The key passed to the function indicates the key of element being transformed.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Map  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.map : ('Key -> 'T -> 'U) -> Map<'Key,'T> -> Map<'Key,'U> (requires comparison)  
  
// Usage:  
Map.map mapping table  
```  
  
#### Parameters  
 `mapping`  
 Type: `'Key -> 'T -> 'U`  
  
 The function to transform the key/value pairs.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Return Value  
 The resulting map of keys and transformed values.  
  
## Remarks  
 This function is named `Map` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use **Map.map**.  
  
 [!CODE [FsMaps#12](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#12)]  
  
 **Output**  
  
 **map [(1, "One"); (2, "Two"); (3, "Three")]**  
**map [(1, "ONE"); (2, "TWO"); (3, "THREE")]**  
**map [(1, "one"); (2, "two"); (3, "three")]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)