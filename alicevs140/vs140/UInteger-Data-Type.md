---
title: "UInteger Data Type"
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
ms.assetid: db7ddd34-4f23-46f5-84dd-8b0f83bb8729
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# UInteger Data Type
Holds unsigned 32-bit (4-byte) integers ranging in value from 0 through 4,294,967,295.  
  
## Remarks  
 The `UInteger` data type provides the largest unsigned value in the most efficient data width.  
  
 The default value of `UInteger` is 0.  
  
## Programming Tips  
 The `UInteger` and `Integer` data types provide optimal performance on a 32-bit processor, because the smaller integer types (`UShort`, `Short`, `Byte`, and `SByte`), even though they use fewer bits, take more time to load, store, and fetch.  
  
-   **Negative Numbers.** Because `UInteger` is an unsigned type, it cannot represent a negative number. If you use the unary minus (`-`) operator on an expression that evaluates to type `UInteger`, Visual Basic converts the expression to `Long` first.  
  
-   **CLS Compliance.** The `UInteger` data type is not part of the [Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6) (CLS), so CLS-compliant code cannot consume a component that uses it.  
  
-   **Interop Considerations.** If you are interfacing with components not written for the .NET Framework, for example Automation or COM objects, keep in mind that types such as `uint` can have a different data width (16 bits) in other environments. If you are passing a 16-bit argument to such a component, declare it as `UShort` instead of `UInteger` in your managed Visual Basic code.  
  
-   **Widening.** The `UInteger` data type widens to `Long`, `ULong`, `Decimal`, `Single`, and `Double`. This means you can convert `UInteger` to any of these types without encountering a <xref:System.OverflowException?qualifyHint=True> error.  
  
-   **Type Characters.** Appending the literal type characters `UI` to a literal forces it to the `UInteger` data type. `UInteger` has no identifier type character.  
  
-   **Framework Type.** The corresponding type in the .NET Framework is the <xref:System.UInt32?qualifyHint=True> structure.  
  
## See Also  
 <xref:System.UInt32?qualifyHint=False>   
 [Data Types](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Conversion Summary](../vs140/Conversion-Summary--Visual-Basic-.md)   
 [How to: Call a Windows Function that Takes Unsigned Types](../vs140/How-to--Call-a-Windows-Function-that-Takes-Unsigned-Types--Visual-Basic-.md)   
 [Efficient Use of Data Types](../Topic/Efficient%20Use%20of%20Data%20Types%20\(Visual%20Basic\).md)