---
title: "Nullable.char&lt;^T&gt; Function (F#)"
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
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 27c61925-0ccd-4f7f-b911-8f656d63eb6f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Nullable.char&lt;^T&gt; Function (F#)
Converts the argument to [char](../Topic/Core.char%20Type%20Abbreviation%20\(F%23\).md). Numeric inputs are converted according to the UTF-16 encoding for characters. The operation requires an appropriate static conversion method on the input type.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.Nullable  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
char : Nullable<^T> -> Nullable<char> when ^T with static member op_Explicit and ^T : (new : unit ->  ^T) and ^T : struct and ^T :> ValueType  
  
// Usage:  
Nullable.char value  
```  
  
#### Parameters  
 `value`  
 Type: <xref:System.Nullable`1?qualifyHint=False><^T>  
  
 The input value.  
  
## Return Value  
 The converted char.  
  
## Remarks  
 This function is named `ToChar` in the .NET assembly. If accessing the member from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Linq.Nullable Module (F#)](../Topic/Linq.Nullable%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)   
 [Operators.char<^T> Function (F#)](../vs140/Operators.char-^T--Function--F#-.md)