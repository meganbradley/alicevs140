---
title: "Map.Add&lt;&#39;Key,&#39;Value&gt; Method (F#)"
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
  - Map.Add<'Key,'Value>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7126bb07-f521-421f-ae84-41e0321f4279
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.Add&lt;&#39;Key,&#39;Value&gt; Method (F#)
Returns a new map with the binding added to the given map.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Add : 'Key * 'Value -> Map<'Key, 'Value> (requires comparison)  
  
// Usage:  
map.Add (key, value)  
```  
  
#### Parameters  
 `key`  
 Type: `'Key`  
  
 The input key.  
  
 `value`  
 Type: `'Value`  
  
 The input value.  
  
## Return Value  
 The resulting map.  
  
## Remarks  
  
## Example  
 The following code example shows how to use the `Add` method.  
  
 [!CODE [FsMaps#2](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#2)]  
  
 **Output**  
  
 **key: 0 value: zero**  
**key: 1 value: one**  
**key: 2 value: two**  
**key: 3 value: three**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map<'Key,'Value> Class (F#)](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)