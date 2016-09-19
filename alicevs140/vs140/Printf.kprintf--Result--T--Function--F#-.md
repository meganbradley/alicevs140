---
title: "Printf.kprintf&lt;&#39;Result,&#39;T&gt; Function (F#)"
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
  - Printf.kprintf<'Result,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fa31f68e-f039-4406-b9e1-688945430124
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Printf.kprintf&lt;&#39;Result,&#39;T&gt; Function (F#)
Like [printf](../vs140/Printf.printf--T--Function--F#-.md), but calls the specified function to generate the result. For example, these let the printing force a flush after all output has been entered onto the channel, but not before.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Printf  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
kprintf : (string -> 'Result) -> StringFormat<'T,'Result> -> 'T  
  
// Usage:  
kprintf continutation format  
```  
  
#### Parameters  
 `continutation`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md) `-> 'Result`  
  
 The function called after formatting to generate the format result.  
  
 `format`  
 Type: [StringFormat](../vs140/Printf.StringFormat--T--Result--Type-Abbreviation--F#-.md)`<'T,'Result>`  
  
 The input formatter.  
  
## Return Value  
 The arguments of the formatter.  
  
## Remarks  
 This function is named `PrintFormatThen` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Printf Module (F#)](../Topic/Core.Printf%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)