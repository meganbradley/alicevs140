---
title: "Printf.ksprintf&lt;&#39;Result,&#39;T&gt; Function (F#)"
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
  - Printf.ksprintf<'Result,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 03e98a01-11af-4f2c-902f-451cfca943e5
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Printf.ksprintf&lt;&#39;Result,&#39;T&gt; Function (F#)
Like [sprintf](../vs140/Printf.sprintf--T--Function--F#-.md), but calls the specified function to generate the result. See [kprintf](../vs140/Printf.kprintf--Result--T--Function--F#-.md).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Printf  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
ksprintf : (string -> 'Result) -> StringFormat<'T,'Result> -> 'T  
  
// Usage:  
ksprintf continutation format  
```  
  
#### Parameters  
 `continutation`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md) `-> 'Result`  
  
 The function called to generate a result from the formatted string.  
  
 `format`  
 Type: [StringFormat](../vs140/Printf.StringFormat--T--Result--Type-Abbreviation--F#-.md)`<'T,'Result>`  
  
 The input formatter.  
  
## Return Value  
 The arguments of the formatter.  
  
## Remarks  
 This function is named `PrintFormatToStringThen` in compiled assemblies. If you are accessing the member from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Printf Module (F#)](../Topic/Core.Printf%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)