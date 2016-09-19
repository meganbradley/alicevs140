---
title: "Map.ofSeq&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.of_seq<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8449a3ef-b5a4-4731-904f-929c8efb1a2f
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.ofSeq&lt;&#39;Key,&#39;T&gt; Function (F#)
Returns a new map made from the given bindings.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Map  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.ofSeq : seq<'Key * 'T> -> Map<'Key,'T> (requires comparison)  
  
// Usage:  
Map.ofSeq elements  
```  
  
#### Parameters  
 `elements`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'Key * 'T>`  
  
 The input sequence of key/value pairs.  
  
## Return Value  
 The resulting map.  
  
## Remarks  
 This function is named `OfSeq` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)