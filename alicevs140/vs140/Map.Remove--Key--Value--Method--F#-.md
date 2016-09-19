---
title: "Map.Remove&lt;&#39;Key,&#39;Value&gt; Method (F#)"
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
  - Map.Remove<'Key,'Value>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 91504235-d9ff-4117-bb40-7d0e11a84ae7
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.Remove&lt;&#39;Key,&#39;Value&gt; Method (F#)
Removes an element from the domain of the map. No exception is raised if the element is not present.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Remove : 'Key -> Map<'Key, 'Value> (requires comparison)  
  
// Usage:  
map.Remove (key)  
```  
  
#### Parameters  
 `key`  
 Type: `'Key`  
  
 The input key.  
  
## Return Value  
 The resulting map.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map<'Key,'Value> Class (F#)](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)