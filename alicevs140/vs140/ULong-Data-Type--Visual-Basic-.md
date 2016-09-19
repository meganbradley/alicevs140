---
title: "ULong Data Type (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 017e0702-774e-44ae-bedc-786b424ca84e
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ULong Data Type (Visual Basic)
Holds unsigned 64-bit (8-byte) integers ranging in value from 0 through 18,446,744,073,709,551,615 (more than 1.84 times 10 ^ 19).  
  
## Remarks  
 Use the `ULong` data type to contain binary data too large for `UInteger`, or the largest possible unsigned integer values.  
  
 The default value of `ULong` is 0.  
  
## Programming Tips  
  
-   **Negative Numbers.** Because `ULong` is an unsigned type, it cannot represent a negative number. If you use the unary minus (`-`) operator on an expression that evaluates to type `ULong`, Visual Basic converts the expression to `Decimal` first.  
  
-   **CLS Compliance.** The `ULong` data type is not part of the [Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6) (CLS), so CLS-compliant code cannot consume a component that uses it.  
  
-   **Interop Considerations.** If you are interfacing with components not written for the .NET Framework, for example Automation or COM objects, keep in mind that types such as `ulong` can have a different data width (32 bits) in other environments. If you are passing a 32-bit argument to such a component, declare it as `UInteger` instead of `ULong` in your managed Visual Basic code.  
  
     Furthermore, Automation does not support 64-bit integers on Windows 95, Windows 98, Windows ME, or Windows 2000. You cannot pass a Visual Basic `ULong` argument to an Automation component on these platforms.  
  
-   **Widening.** The `ULong` data type widens to `Decimal`, `Single`, and `Double`. This means you can convert `ULong` to any of these types without encountering a <xref:System.OverflowException?qualifyHint=True> error.  
  
-   **Type Characters.** Appending the literal type characters `UL` to a literal forces it to the `ULong` data type. `ULong` has no identifier type character.  
  
-   **Framework Type.** The corresponding type in the .NET Framework is the <xref:System.UInt64?qualifyHint=True> structure.  
  
## See Also  
 <xref:System.UInt64?qualifyHint=False>   
 [Data Types](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Conversion Summary](../vs140/Conversion-Summary--Visual-Basic-.md)   
 [How to: Call a Windows Function that Takes Unsigned Types](../vs140/How-to--Call-a-Windows-Function-that-Takes-Unsigned-Types--Visual-Basic-.md)   
 [Efficient Use of Data Types](../Topic/Efficient%20Use%20of%20Data%20Types%20\(Visual%20Basic\).md)