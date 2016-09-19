---
title: "Seq.head&lt;&#39;T&gt; Function (F#)"
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
  - Seq.hd<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 75a3053e-4c20-4f6e-8347-3673c147517c
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.head&lt;&#39;T&gt; Function (F#)
Returns the first element of the sequence.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.head : seq<'T> -> 'T  
  
// Usage:  
Seq.head source  
```  
  
#### Parameters  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input sequence.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the input does not have any elements.|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when the input sequence is null.|  
  
## Return Value  
 The first element of the sequence.  
  
## Remarks  
 The first element of the `source` sequence is evaluated at each call. To avoid this reevaluation, you can create a cached version of a sequence by calling [Seq.cache](../vs140/Seq.cache--T--Function--F#-.md).  
  
 This function is named `Head` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Seq.head`.  
  
 [!CODE [FsSequences#41](../CodeSnippet/VS_Snippets_Fsharp/fssequences#41)]  
  
 **Output**  
  
 **1**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)