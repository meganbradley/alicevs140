---
title: "Printf.sprintf&lt;&#39;T&gt; Function (F#)"
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
  - Printf.sprintf<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d66bc456-582f-48ec-8054-ca48d99d6ffd
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Printf.sprintf&lt;&#39;T&gt; Function (F#)
Prints to a string via an internal string buffer and returns the result as a string. Helper printers must return strings.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Printf  
  
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
  
 The input formatter.  
  
## Return Value  
 The formatted string.  
  
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