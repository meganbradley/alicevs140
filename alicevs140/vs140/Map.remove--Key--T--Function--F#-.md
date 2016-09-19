---
title: "Map.remove&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.remove<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fa512ed2-dce1-499d-b4c6-7d71d5c767e2
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.remove&lt;&#39;Key,&#39;T&gt; Function (F#)
Removes an element from the domain of the map. No exception is raised if the element is not present.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Map  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.remove : 'Key -> Map<'Key,'T> -> Map<'Key,'T> (requires comparison)  
  
// Usage:  
Map.remove key table  
```  
  
#### Parameters  
 `key`  
 Type: `'Key`  
  
 The input key.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Return Value  
 The resulting map.  
  
## Remarks  
 This function is named `Remove` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)