---
title: "Printf.printfn&lt;&#39;T&gt; Function (F#)"
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
  - Printf.printfn<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ec1e8178-0caa-453c-9bdd-e48519401e0d
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Printf.printfn&lt;&#39;T&gt; Function (F#)
Prints formatted output to `stdout`, adding a newline.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Printf  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
printfn : TextWriterFormat<'T> -> 'T  
  
// Usage:  
printfn format  
```  
  
#### Parameters  
 `format`  
 Type: [TextWriterFormat](../vs140/Printf.TextWriterFormat--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input formatter.  
  
## Return Value  
 The return type and arguments of the formatter.  
  
## Remarks  
 This function is named `PrintFormatLine` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0  
  
## See Also  
 [Core.Printf Module (F#)](../Topic/Core.Printf%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)