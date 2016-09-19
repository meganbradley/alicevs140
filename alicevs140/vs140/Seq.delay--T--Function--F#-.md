---
title: "Seq.delay&lt;&#39;T&gt; Function (F#)"
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
  - Seq.delay<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 984c6349-4970-4945-9443-43fc1a3a46e5
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.delay&lt;&#39;T&gt; Function (F#)
Returns a sequence that is built from the given delayed specification of a sequence.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.delay : (unit -> seq<'T>) -> seq<'T>  
  
// Usage:  
Seq.delay generator  
```  
  
#### Parameters  
 `generator`  
 Type: [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md) `->` [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The generating function for the sequence.  
  
## Return Value  
 The resulting sequence.  
  
## Remarks  
 The input function is evaluated each time an `IEnumerator` for the sequence is requested.  
  
 This function is named `Delay` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Seq.delay` to delay the evaluation of a sequence that is created from a collection that is normally evaluated immediately.  
  
 [!CODE [FsSequences#30](../CodeSnippet/VS_Snippets_Fsharp/fssequences#30)]  
  
 **Output**  
  
 **Calling makeSequence.**  
**Printing sequences.**  
**Squares:**  
**Evaluating 4.**  
**Evaluating 3.**  
**Evaluating 2.**  
**Evaluating 1.**  
**Evaluating 0.16 9 4 1 Cubes:Evaluating 4.**  
**Evaluating 3.**  
**Evaluating 2.**  
**Evaluating 1.**  
**Evaluating 0.**  
**64 27 8 1**   
## Example  
 The following code example is equivalent to the previous example, except that it does not use `Seq.delay`. Notice the difference in the output.  
  
 [!CODE [FsSequences#31](../CodeSnippet/VS_Snippets_Fsharp/fssequences#31)]  
  
 **Output**  
  
 **Calling makeSequence.**  
**Evaluating 4.**  
**Evaluating 3.**  
**Evaluating 2.**  
**Evaluating 1.**  
**Evaluating 0.**  
**Evaluating 4.**  
**Evaluating 3.**  
**Evaluating 2.**  
**Evaluating 1.**  
**Evaluating 0.**  
**Printing sequences.**  
**Squares:**  
**16 9 4 1**   
**Cubes:**  
**64 27 8 1**    
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)