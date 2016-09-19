---
title: "Map.tryPick&lt;&#39;Key,&#39;T,&#39;U&gt; Function (F#)"
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
  - Map.tryPick<'Key,'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 71f66885-1aad-4363-9527-5f9856e6cee9
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.tryPick&lt;&#39;Key,&#39;T,&#39;U&gt; Function (F#)
Searches the map looking for the first element where the given function returns a `Some` value.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Map  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.tryPick : ('Key -> 'T -> 'U option) -> Map<'Key,'T> -> 'U option (requires comparison)  
  
// Usage:  
Map.tryPick chooser table  
```  
  
#### Parameters  
 `chooser`  
 Type: `'Key -> 'T -> 'U`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The function to generate options from the key/value pairs.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Return Value  
 The first result.  
  
## Remarks  
 This function is named `TryPick` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows the use of the `Map.tryPick` function.  
  
 [!CODE [FsMaps#18](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#18)]  
  
 **Output**  
  
 **Result where key and value are the same: 50**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)