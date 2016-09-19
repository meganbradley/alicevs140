---
title: "Map.ContainsKey&lt;&#39;Key,&#39;Value&gt; Method (F#)"
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
  - Map.ContainsKey<'Key,'Value>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 02b7326c-f089-4b0d-8f6b-df8fd7aa2532
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.ContainsKey&lt;&#39;Key,&#39;Value&gt; Method (F#)
Tests if an element is in the domain of the map.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.ContainsKey : 'Key -> bool (requires comparison)  
  
// Usage:  
map.ContainsKey (key)  
```  
  
#### Parameters  
 `key`  
 Type: `'Key`  
  
 The input key.  
  
## Return Value  
 `true` if the map contains the given key.  
  
## Remarks  
  
## Example  
 The following code shows how to use the `ContainsKey` method.  
  
 [!CODE [FsMaps#4](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#4)]  
  
 **Output**  
  
 **The specified map contains the key 1.**  
**The specified map does not contain the key 0.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map<'Key,'Value> Class (F#)](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)