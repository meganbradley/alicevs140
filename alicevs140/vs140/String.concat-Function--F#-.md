---
title: "String.concat Function (F#)"
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
  - String.concat
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a66f19e5-2002-4960-8ce8-eae1be77bc5f
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# String.concat Function (F#)
Returns a new string made by concatenating the given strings with a separator.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.String  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
String.concat : string -> seq<string> -> string  
  
// Usage:  
String.concat sep strings  
```  
  
#### Parameters  
 `sep`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The separator string to be inserted between the strings of the input sequence.  
  
 `strings`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<`[string](../vs140/Core.string-Type-Abbreviation--F#-.md)`>`  
  
 The sequence of strings to be concatenated.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when strings is null.|  
  
## Return Value  
 A new string consisting of the concatenated strings separated by the separation string.  
  
## Remarks  
 This function is named `Concat` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `String.concat`.  
  
 [!CODE [FsStrings#2](../CodeSnippet/VS_Snippets_Fsharp/fsstrings#2)]  
  
 **Output**  
  
 **tomatoes, bananas, apples**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.String Module (F#)](../Topic/Core.String%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)