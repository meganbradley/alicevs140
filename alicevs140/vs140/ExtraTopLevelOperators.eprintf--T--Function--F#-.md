---
title: "ExtraTopLevelOperators.eprintf&lt;&#39;T&gt; Function (F#)"
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
  - ExtraTopLevelOperators.eprintf<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 501be259-4adc-414e-bc7b-0f665c777fd4
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ExtraTopLevelOperators.eprintf&lt;&#39;T&gt; Function (F#)
Print to `stderr` using the given format.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.ExtraTopLevelOperators  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
eprintf : TextWriterFormat<'T> -> 'T  
  
// Usage:  
eprintf format  
```  
  
#### Parameters  
 `format`  
 Type: [TextWriterFormat](../vs140/Printf.TextWriterFormat--T--Type-Abbreviation--F#-.md)`<'T>`  
  
## Return Value  
  
## Remarks  
 This function is named `PrintFormatToError` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example demonstrates the use of `eprintf`.  
  
 [!CODE [FsCoreLib2#2](../CodeSnippet/VS_Snippets_Fsharp/fscorelib2#2)]  
  
 The output is as follows.  
  
 **Success!**  
**Error: the input 11 exceeds the maximum value 10.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0  
  
## See Also  
 [Core.ExtraTopLevelOperators Module (F#)](../Topic/Core.ExtraTopLevelOperators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)