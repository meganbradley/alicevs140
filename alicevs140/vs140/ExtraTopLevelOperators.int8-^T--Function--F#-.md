---
title: "ExtraTopLevelOperators.int8&lt;^T&gt; Function (F#)"
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
  - ExtraTopLevelOperators.int8<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e42d6978-87f1-41af-a535-e138ddd90085
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ExtraTopLevelOperators.int8&lt;^T&gt; Function (F#)
Converts the argument to signed byte. This is a direct conversion for all primitive numeric types. For strings, the input is converted using <xref:System.SByte.Parse?qualifyHint=False> with <xref:System.Globalization.CultureInfo.InvariantCulture?qualifyHint=False> settings. Otherwise the operation requires and invokes a `ToSByte` method on the input type  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.ExtraTopLevelOperators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
int8 : ^T -> sbyte (requires ^T with static member op_Explicit)  
  
// Usage:  
int8 value  
```  
  
#### Parameters  
 `value`  
 Type: `^T`  
  
 The value to convert.  
  
## Return Value  
 The converted value of type [sbyte](../Topic/Core.sbyte%20Type%20Abbreviation%20\(F%23\).md).  
  
## Remarks  
 This function is named `ToSByte` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.ExtraTopLevelOperators Module (F#)](../Topic/Core.ExtraTopLevelOperators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)