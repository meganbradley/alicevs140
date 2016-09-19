---
title: "Set.ofSeq&lt;&#39;T&gt; Function (F#)"
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
  - Set.of_seq<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 5e8b5b4e-2d88-49bf-b74a-cf3ef553a888
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.ofSeq&lt;&#39;T&gt; Function (F#)
Creates a new collection from the given enumerable object.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Set  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.ofSeq : seq<'T> -> Set<'T> (requires comparison)  
  
// Usage:  
Set.ofSeq elements  
```  
  
#### Parameters  
 `elements`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input sequence.  
  
## Return Value  
 The set containing `elements`.  
  
## Remarks  
 This function is named `OfSeq` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates how to create a set from a sequence by using `Set.ofSeq`.  
  
 [!CODE [FsSamples101#2001](../CodeSnippet/VS_Snippets_Fsharp/fssamples101#2001)]  
  
 **' ' 'T' 'a' 'b' 'c' 'd' 'e' 'f' 'g' 'h' 'i' 'j' 'k' 'l' 'm' 'n' 'o' 'p' 'q' 'r' 's' 't' 'u' 'v' 'w' 'x' 'y' 'z'**    
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)