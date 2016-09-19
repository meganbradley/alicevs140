---
title: "ExtraTopLevelOperators.sprintf&lt;&#39;T&gt; Function (F#)"
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
  - ExtraTopLevelOperators.sprintf<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8ddc0cc1-4e80-4371-820d-cdde04ab8145
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ExtraTopLevelOperators.sprintf&lt;&#39;T&gt; Function (F#)
The sprintf function prints to a string using the given format.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.ExtraTopLevelOperators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
sprintf : StringFormat<'T> -> 'T  
  
// Usage:  
sprintf format  
```  
  
#### Parameters  
 `format`  
 Type: [StringFormat](../vs140/Printf.StringFormat--T--Type-Abbreviation--F#-.md)`<'T>`  
  
## Return Value  
  
## Remarks  
 This function is named `PrintFormatToString` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `sprintf`.  
  
 [!CODE [FsCoreLib2#10](../CodeSnippet/VS_Snippets_Fsharp/fscorelib2#10)]  
  
 **Formatted string with value 109...**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.ExtraTopLevelOperators Module (F#)](../Topic/Core.ExtraTopLevelOperators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)