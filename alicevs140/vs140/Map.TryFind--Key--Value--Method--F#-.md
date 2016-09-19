---
title: "Map.TryFind&lt;&#39;Key,&#39;Value&gt; Method (F#)"
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
  - Map.TryFind<'Key,'Value>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a282a8bb-65aa-4bca-94e1-7d239ca12edc
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.TryFind&lt;&#39;Key,&#39;Value&gt; Method (F#)
Lookup an element in the map, returning a `Some` value if the element is in the domain of the map and `None` if not.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.TryFind : 'Key -> 'Value option (requires comparison)  
  
// Usage:  
map.TryFind (key)  
```  
  
#### Parameters  
 `key`  
 Type: `'Key`  
  
 The input key.  
  
## Return Value  
 The mapped value, or `None` if the key is not in the map.  
  
## Remarks  
  
## Example  
 The following code shows how to use the `TryFind` method.  
  
 [!CODE [FsMaps#16](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#16)]  
  
 **Output**  
  
 **Found 2500.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map<'Key,'Value> Class (F#)](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)