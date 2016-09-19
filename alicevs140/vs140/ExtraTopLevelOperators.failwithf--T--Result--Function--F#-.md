---
title: "ExtraTopLevelOperators.failwithf&lt;&#39;T,&#39;Result&gt; Function (F#)"
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
  - ExtraTopLevelOperators.failwithf<'T,'Result>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 677781f0-fb69-4dfe-9d18-8fb1a7fc7aed
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ExtraTopLevelOperators.failwithf&lt;&#39;T,&#39;Result&gt; Function (F#)
Print to a string buffer and raise an exception with the given result. Helper printers must return strings.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.ExtraTopLevelOperators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
failwithf : StringFormat<'T,'Result> -> 'T  
  
// Usage:  
failwithf format  
```  
  
#### Parameters  
 `format`  
 Type: [StringFormat](../vs140/Printf.StringFormat--T--Result--Type-Abbreviation--F#-.md)`<'T,'Result>`  
  
## Return Value  
  
## Remarks  
 This function is named `PrintFormatToStringThenFail` in compiled assemblies. If you are accessing the member from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `failwithf`.  
  
 [!CODE [FsCoreLib2#4](../CodeSnippet/VS_Snippets_Fsharp/fscorelib2#4)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.ExtraTopLevelOperators Module (F#)](../Topic/Core.ExtraTopLevelOperators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)