---
title: "String.iter Function (F#)"
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
  - String.iter
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: dad84486-fe93-4475-aea6-8735d463ac4d
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# String.iter Function (F#)
Applies a specified function to each character in a string.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.String  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
String.iter : (char -> unit) -> string -> unit  
  
// Usage:  
String.iter action str  
```  
  
#### Parameters  
 `action`  
 Type: [char](../Topic/Core.char%20Type%20Abbreviation%20\(F%23\).md) `->` [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 The function to be applied to each character of the string.  
  
 `str`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The input string.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when the input string is null.|  
  
## Remarks  
 This function is named `Iterate` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.String Module (F#)](../Topic/Core.String%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)