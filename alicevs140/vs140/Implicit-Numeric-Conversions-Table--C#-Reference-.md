---
title: "Implicit Numeric Conversions Table (C# Reference)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implicit Numeric Conversions Table (C# Reference)
The following table shows the predefined implicit numeric conversions. Implicit conversions might occur in many situations, including method invoking and assignment statements.  
  
|From|To|  
|----------|--------|  
|[sbyte](../Topic/sbyte%20\(C%23%20Reference\).md)|`short`, `int`, `long`, `float`, `double`, or `decimal`|  
|[byte](../Topic/byte%20\(C%23%20Reference\).md)|`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`|  
|[short](../Topic/short%20\(C%23%20Reference\).md)|`int`, `long`, `float`, `double`, or `decimal`|  
|[ushort](../Topic/ushort%20\(C%23%20Reference\).md)|`int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`|  
|[int](../Topic/int%20\(C%23%20Reference\).md)|`long`, `float`, `double`, or `decimal`|  
|[uint](../Topic/uint%20\(C%23%20Reference\).md)|`long`, `ulong`, `float`, `double`, or `decimal`|  
|[long](../vs140/long--C#-Reference-.md)|`float`, `double`, or `decimal`|  
|[char](../vs140/char--C#-Reference-.md)|`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`|  
|[float](../vs140/float--C#-Reference-.md)|`double`|  
|[ulong](../Topic/ulong%20\(C%23%20Reference\).md)|`float`, `double`, or `decimal`|  
  
## Remarks  
  
-   Precision but not magnitude might be lost in the conversions from `int`, `uint`,  `long`, or `ulong` to `float` and from `long` or `ulong` to `double`.  
  
-   There are no implicit conversions to the `char` type.  
  
-   There are no implicit conversions between floating-point types and the `decimal` type.  
  
-   A constant expression of type `int` can be converted to `sbyte`, `byte`, `short`, `ushort`, `uint`, or `ulong`, provided the value of the constant expression is within the range of the destination type.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Integral Types Table](../vs140/Integral-Types-Table--C#-Reference-.md)   
 [Built-in Types Table (Visual C#)](../Topic/Built-In%20Types%20Table%20\(C%23%20Reference\).md)   
 [Explicit Numeric Conversions Table (Visual C#)](../Topic/Explicit%20Numeric%20Conversions%20Table%20\(C%23%20Reference\).md)   
 [Casting and Type Conversions (C# Programming Guide)](../Topic/Casting%20and%20Type%20Conversions%20\(C%23%20Programming%20Guide\).md)