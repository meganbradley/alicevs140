---
title: "Map.toSeq&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.to_seq<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 32646074-6c9b-4813-8b53-77317b950d8e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.toSeq&lt;&#39;Key,&#39;T&gt; Function (F#)
Views the collection as an enumerable sequence of pairs. The sequence will be ordered by the keys of the map.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Map  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.toSeq : Map<'Key,'T> -> seq<'Key * 'T> (requires comparison)  
  
// Usage:  
Map.toSeq table  
```  
  
#### Parameters  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Return Value  
 The sequence of key/value pairs.  
  
## Remarks  
 This function is named `ToSeq` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)