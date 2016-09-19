---
title: "Map.ofList&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.of_list<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: baa7df23-d015-44b0-8f20-f4a3631dcc8f
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.ofList&lt;&#39;Key,&#39;T&gt; Function (F#)
Returns a new map made from the given bindings.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Map  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.ofList : 'Key * 'T list -> Map<'Key,'T> (requires comparison)  
  
// Usage:  
Map.ofList elements  
```  
  
#### Parameters  
 `elements`  
 Type: `'Key * 'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list of key/value pairs.  
  
## Return Value  
 The resulting map.  
  
## Remarks  
 This function is named `OfList` in compiled assemblies. If accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)