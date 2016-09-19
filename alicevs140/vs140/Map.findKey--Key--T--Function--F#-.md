---
title: "Map.findKey&lt;&#39;Key,&#39;T&gt; Function (F#)"
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
  - Map.findKey<'Key,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 34052cc7-a792-476a-8d66-1764493335e3
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Map.findKey&lt;&#39;Key,&#39;T&gt; Function (F#)
Evaluates the function on each mapping in the collection and returns the key for the first mapping where the function returns `true`. If no such element exists, this function raises <xref:System.Collections.Generic.KeyNotFoundException?qualifyHint=False>.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Map  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Map.findKey : ('Key -> 'T -> bool) -> Map<'Key,'T> -> 'Key (requires comparison)  
  
// Usage:  
Map.findKey predicate table  
```  
  
#### Parameters  
 `predicate`  
 Type: `'Key -> 'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `table`  
 Type: [Map](../Topic/Collections.Map%3C'Key,'Value%3E%20Class%20\(F%23\).md)`<'Key,'T>`  
  
 The input map.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.Collections.Generic.KeyNotFoundException?qualifyHint=False>|Thrown if the key does not exist in the map.|  
  
## Return Value  
 The first key for which the predicate evaluates `true`.  
  
## Remarks  
 This function is named `FindKey` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example shows how to use `Map.findKey`.  
  
 [!CODE [FsMaps#7](../CodeSnippet/VS_Snippets_Fsharp/fsmaps#7)]  
  
 **Output**  
  
 **With value "one", found key 1.**  
**With value "two", found key 2.**  
**With value 9, found key 3.**  
**With value 25, found key 5.**  
**Exception of type 'System.Collections.Generic.KeyNotFoundException' was thrown.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Map Module (F#)](../vs140/Collections.Map-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)