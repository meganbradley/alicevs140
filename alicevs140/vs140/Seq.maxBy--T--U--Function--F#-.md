---
title: "Seq.maxBy&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Seq.maxBy<'T,'Key>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 64740cf8-c8d7-4880-a38c-2eeb2ea3b2bb
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.maxBy&lt;&#39;T,&#39;U&gt; Function (F#)
Returns the greatest of all elements of the sequence, compared by using [Operators.max](../vs140/Operators.max--T--Function--F#-.md) on the function result.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.maxBy : ('T -> 'U) -> seq<'T> -> 'T (requires comparison)  
  
// Usage:  
Seq.maxBy projection source  
```  
  
#### Parameters  
 `projection`  
 Type: `'T -> 'U`  
  
 A function to transform items from the input sequence into comparable keys.  
  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input sequence.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the input sequence is empty.|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when the input sequence is null.|  
  
## Return Value  
 The result sequence.  
  
## Remarks  
 This function is named `MaxBy` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)