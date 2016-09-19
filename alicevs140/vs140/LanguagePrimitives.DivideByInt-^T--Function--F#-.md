---
title: "LanguagePrimitives.DivideByInt&lt;^T&gt; Function (F#)"
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
  - LanguagePrimitives.DivideByInt<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 24b70b03-c9fb-4edf-b04e-c9d8355fe1ca
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LanguagePrimitives.DivideByInt&lt;^T&gt; Function (F#)
Divides a value by an integer.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
DivideByInt : ^T -> int -> ^T (requires ^T with static member DivideByInt)  
  
// Usage:  
DivideByInt x y  
```  
  
#### Parameters  
 `x`  
 Type: `^T`  
  
 The dividend, or numerator.  
  
 `y`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The divisor, or denominator.  
  
## Return Value  
 The quotient.  
  
## Remarks  
 If a type supports `DivideByInt`, the type supports exact division (floating-point division), rather than integer division, which rounds down to the nearest integer result.  
  
 Functions like [Seq.average](../Topic/Seq.average%3C%5ET%3E%20Function%20\(F%23\).md) work only if the element type supports exact division. If you try to use `Seq.average` with an integer sequence, you get an error that indicates that the element type must implement `DivideByInt`. Typically, you can resolve this error by using [Seq.averageBy](../Topic/Seq.averageBy%3C'T,%5EU%3E%20Function%20\(F%23\).md) and adding a cast to a floating-point value. The following code shows how to use `Seq.averageBy` with an integer sequence.  
  
```f#  
let average = [ 1 .. 10 ]  
              |> Seq.averageBy (fun elem -> float elem)  
printfn "%f" average   
```  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library VersionsF# Core Library Versions**  
  
 Supported in: 2.0, 4.0, PortablePortable2.0, 4.0, Portable  
  
## See Also  
 [Core.LanguagePrimitives Module (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)