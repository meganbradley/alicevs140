---
title: "Map.add&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.add<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8cd69deb-e5c2-4e24-b63f-02b807d3e98d
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.add&lt;&#39;Key,&#39;T&gt; Function (F#)
Returns a new map with the binding added to the given map.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Map  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.add : 'Key -> 'T -> Map<'Key,'T> -> Map<'Key,'T> (requires comparison)  
  
// Usage:  
Map.add key value table  
```  
  
#### Parameters  
 `key`  
 Type: `'Key`  
  
 The input key.  
  
 `value`  
 Type: `'T`  
  
 The input value.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Return Value  
 The resulting map.  
  
## Remarks  
 This function is named `Add` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example shows how to use `Map.add`.  
  
 [!CODE [FsMaps#1](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#1)]  
  
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
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)