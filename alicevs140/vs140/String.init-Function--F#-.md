---
title: "String.init Function (F#)"
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
  - String.init
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2d42d3cd-a278-4dbf-8db5-c9433e312b08
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# String.init Function (F#)
Creates a new string whose characters are the results of applying a specified function to each index and concatenating the resulting strings.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.String  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
String.init : int -> (int -> string) -> string  
  
// Usage:  
String.init count initializer  
```  
  
#### Parameters  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of strings to initialize.  
  
 `initializer`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->` [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The function to take an index and produce a string to be concatenated with the others.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when `count` is negative.|  
  
## Return Value  
 The constructed string.  
  
## Remarks  
 This function is named `Initialize` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `String.init`.  
  
 [!CODE [FsStrings#5](../CodeSnippet/VS_Snippets_Fsharp/fsstrings#5)]  
  
 **Output**  
  
 **0123456789**  
**ABCDEFGHIJKLMNOPQRSTUVWXYZ**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.String Module (F#)](../Topic/Core.String%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)