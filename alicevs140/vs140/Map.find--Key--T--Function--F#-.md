---
title: "Map.find&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.find<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fc984657-9e0f-4544-b7d1-da6572b5ae74
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.find&lt;&#39;Key,&#39;T&gt; Function (F#)
Looks up an element in the map. If no binding exists in the map, raises <xref:System.Collections.Generic.KeyNotFoundException?qualifyHint=False>.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Map  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.find : 'Key -> Map<'Key,'T> -> 'T (requires comparison)  
  
// Usage:  
Map.find key table  
```  
  
#### Parameters  
 `key`  
 Type: `'Key`  
  
 The input key.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.Collections.Generic.KeyNotFoundException?qualifyHint=False>|Thrown when the key does not exist in the map.|  
  
## Return Value  
 The value mapped to the given key.  
  
## Remarks  
 This function is named `Find` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following examples shows how to use `Map.filter`.  
  
 [!CODE [FsMaps#6](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#6)]  
  
 **Output**  
  
 **With key 1, found value "one".**  
**With key 2, found value "two".**  
**With key 3, found value 9.**  
**With key 5, found value 25.**  
**The given key was not present in the dictionary.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)