---
title: "Printf.fprintfn&lt;&#39;T&gt; Function (F#)"
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
  - Printf.fprintfn<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f927a4fa-122c-4547-a87d-6dca9197c4e3
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Printf.fprintfn&lt;&#39;T&gt; Function (F#)
Prints to a text writer, adding a newline.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Printf  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
fprintfn : TextWriter -> TextWriterFormat<'T> -> 'T  
  
// Usage:  
fprintfn textWriter format  
```  
  
#### Parameters  
 `textWriter`  
 Type: <xref:System.IO.TextWriter?qualifyHint=False>  
  
 The <xref:System.IO.TextWriter?qualifyHint=False> instance to print to.  
  
 `format`  
 Type: [TextWriterFormat](../vs140/Printf.TextWriterFormat--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input formatter.  
  
## Return Value  
 The return type and arguments of the formatter.  
  
## Remarks  
 This function is named `PrintFormatLineToTextWriter` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Printf Module (F#)](../Topic/Core.Printf%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)