---
title: "Seq.windowed&lt;&#39;T&gt; Function (F#)"
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
  - Seq.windowed<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8b565b8f-d645-4dba-be22-099075fe4744
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.windowed&lt;&#39;T&gt; Function (F#)
Returns a sequence that yields sliding windows of containing elements drawn from the input sequence. Each window is returned as a fresh array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Seq  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.windowed : int -> seq<'T> -> seq<'T []>  
  
// Usage:  
Seq.windowed windowSize source  
```  
  
#### Parameters  
 `windowSize`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of elements in each window.  
  
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
 This function is named `Windowed` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `Seq.windowed` as part of a computation of a moving average for a sequence of numbers.  
  
 [!CODE [FsSequences#180](../CodeSnippet/VS_Snippets_Fsharp/fssequences#180)]  
  
 **Initial sequence:**   
**1.0 1.5 2.0 1.5 1.0 1.5**   
**Windows of length 3:**   
**[&#124;1.0; 1.5; 2.0&#124;] [&#124;1.5; 2.0; 1.5&#124;] [&#124;2.0; 1.5; 1.0&#124;] [&#124;1.5; 1.0; 1.5&#124;]**   
**Moving average:**   
**1.5 1.666666667 1.5 1.333333333**    
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)