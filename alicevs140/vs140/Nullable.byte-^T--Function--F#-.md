---
title: "Nullable.byte&lt;^T&gt; Function (F#)"
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
ms.assetid: 9d0fd2ef-8b80-44a7-b504-a6e9105035a8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Nullable.byte&lt;^T&gt; Function (F#)
Converts the argument to [byte](../Topic/Core.byte%20Type%20Abbreviation%20\(F%23\).md). This is a direct conversion for all primitive numeric types. The operation requires an appropriate static conversion method on the input type.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.Nullable  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
byte : Nullable<^T> -> Nullable<byte> when ^T with static member op_Explicit and ^T : (new : unit ->  ^T) and ^T : struct and ^T :> ValueType  
  
// Usage:  
Nullable.byte value  
```  
  
#### Parameters  
 `value`  
 Type: <xref:System.Nullable`1?qualifyHint=False><^T>  
  
 The input value.  
  
## Return Value  
 The converted byte.  
  
## Remarks  
 This function is named `ToByte` in the .NET assembly. If accessing the member from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Linq.Nullable Module (F#)](../Topic/Linq.Nullable%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)   
 [Operators.byte<^T> Function (F#)](../Topic/Operators.byte%3C%5ET%3E%20Function%20\(F%23\).md)