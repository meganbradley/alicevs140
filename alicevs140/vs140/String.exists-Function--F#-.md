---
title: "String.exists Function (F#)"
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
  - String.exists
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2a9952a0-7071-4d8f-b32b-90736d5aa781
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# String.exists Function (F#)
Tests if any character of the string satisfies the given predicate.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.String  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
String.exists : (char -> bool) -> string -> bool  
  
// Usage:  
String.exists predicate str  
```  
  
#### Parameters  
 `predicate`  
 Type: [char](../Topic/Core.char%20Type%20Abbreviation%20\(F%23\).md) `->` [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test each character of the string.  
  
 `str`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The input string.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when the input string is null.|  
  
## Return Value  
 Returns `true` if any character returns `true` for the predicate and `false` otherwise.  
  
## Remarks  
 This function is named `Exists` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `String.exists`.  
  
 [!CODE [FsStrings#3](../CodeSnippet/VS_Snippets_Fsharp/fsstrings#3)]  
  
 **Output**  
  
 **The string "Hello World!" contains uppercase characters.**  
**The string "no" does not contain uppercase characters.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.String Module (F#)](../Topic/Core.String%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)