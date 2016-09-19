---
title: "Seq.ofList&lt;&#39;T&gt; Function (F#)"
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
  - Seq.of_list<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f13256ad-a566-4818-824e-1ae70768f95f
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.ofList&lt;&#39;T&gt; Function (F#)
Views the given list as a sequence.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.ofList : 'T list -> seq<'T>  
  
// Usage:  
Seq.ofList source  
```  
  
#### Parameters  
 `source`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The result sequence.  
  
## Remarks  
 This function is named `OfList` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Seq.ofList`.  
  
 [!CODE [FsSequences#61](../CodeSnippet/VS_Snippets_Fsharp/fssequences#61)]  
  
 **F# Interactive Output**  
  
 **val seq1 : seq<string\> = ["0"; "1"; "2"; "3"; "4"; "5"; "6"; "7"; "8"; "9"]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)