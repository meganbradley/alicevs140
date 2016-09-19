---
title: "Map.containsKey&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.containsKey<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 45364a26-984c-4cf8-844f-dad1121c012d
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.containsKey&lt;&#39;Key,&#39;T&gt; Function (F#)
Tests if an element is in the domain of the map.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Map  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.containsKey : 'Key -> Map<'Key,'T> -> bool (requires comparison)  
  
// Usage:  
Map.containsKey key table  
```  
  
#### Parameters  
 `key`  
 Type: `'Key`  
  
 The input key.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Return Value  
 `true` if the map contains the key.  
  
## Remarks  
 This function is named `ContainsKey` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Map.containsKey`.  
  
 [!CODE [FsMaps#3](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#3)]  
  
 **Output**  
  
 **The specified map contains the key 1.**  
**The specified map does not contain the key 0.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)