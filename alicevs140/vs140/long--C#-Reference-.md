---
title: "long (C# Reference)"
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
ms.assetid: f9b24319-1f39-48be-a42b-d528ee28a7fd
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# long (C# Reference)
The `long` keyword denotes an integral type that stores values according to the size and range shown in the following table.  
  
|Type|Range|Size|.NET Framework type|  
|----------|-----------|----------|-------------------------|  
|`long`|–9,223,372,036,854,775,808 to 9,223,372,036,854,775,807|Signed 64-bit integer|<xref:System.Int64?qualifyHint=True>|  
  
## Literals  
 You can declare and initialize a `long` variable like this example:  
  
```  
  
long long1 = 4294967296;  
```  
  
 When an integer literal has no suffix, its type is the first of these types in which its value can be represented: [int](../Topic/int%20\(C%23%20Reference\).md), [uint](../Topic/uint%20\(C%23%20Reference\).md), `long`, [ulong](../Topic/ulong%20\(C%23%20Reference\).md). In the preceding example, it is of the type `long` because it exceeds the range of [uint](../Topic/uint%20\(C%23%20Reference\).md) (see [Integral Types Table](../vs140/Integral-Types-Table--C#-Reference-.md) for the storage sizes of integral types).  
  
 You can also use the suffix L with the `long` type like this:  
  
```  
  
long long2 = 4294967296L;  
```  
  
 When you use the suffix L, the type of the literal integer is determined to be either `long` or [ulong](../Topic/ulong%20\(C%23%20Reference\).md) according to its size. In the case it is `long` because it less than the range of [ulong](../Topic/ulong%20\(C%23%20Reference\).md).  
  
 A common use of the suffix is with calling overloaded methods. Consider, for example, the following overloaded methods that use `long` and [int](../Topic/int%20\(C%23%20Reference\).md) parameters:  
  
```  
public static void SampleMethod(int i) {}  
public static void SampleMethod(long l) {}  
```  
  
 Using the suffix L guarantees that the correct type is called, for example:  
  
```  
SampleMethod(5);    // Calling the method with the int parameter  
SampleMethod(5L);   // Calling the method with the long parameter  
```  
  
 You can use the `long` type with other numeric integral types in the same expression, in which case the expression is evaluated as `long` (or [bool](../Topic/bool%20\(C%23%20Reference\).md) in the case of relational or Boolean expressions). For example, the following expression evaluates as `long`:  
  
```  
898L + 88  
```  
  
> [!NOTE]
>  You can also use the lowercase letter "l" as a suffix. However, this generates a compiler warning because the letter "l" is easily confused with the digit "1." Use "L" for clarity.  
  
 For information on arithmetic expressions with mixed floating-point types and integral types, see [float](../vs140/float--C#-Reference-.md) and [double](../vs140/double--C#-Reference-.md).  
  
## Conversions  
 There is a predefined implicit conversion from `long` to [float](../vs140/float--C#-Reference-.md), [double](../vs140/double--C#-Reference-.md), or [decimal](../Topic/decimal%20\(C%23%20Reference\).md). Otherwise a cast must be used. For example, the following statement will produce a compilation error without an explicit cast:  
  
```  
int x = 8L;        // Error: no implicit conversion from long to int  
int x = (int)8L;   // OK: explicit conversion to int  
```  
  
 There is a predefined implicit conversion from [sbyte](../Topic/sbyte%20\(C%23%20Reference\).md), [byte](../Topic/byte%20\(C%23%20Reference\).md), [short](../Topic/short%20\(C%23%20Reference\).md), [ushort](../Topic/ushort%20\(C%23%20Reference\).md), [int](../Topic/int%20\(C%23%20Reference\).md), [uint](../Topic/uint%20\(C%23%20Reference\).md), or [char](../vs140/char--C#-Reference-.md) to `long`.  
  
 Notice also that there is no implicit conversion from floating-point types to `long`. For example, the following statement generates a compiler error unless an explicit cast is used:  
  
```  
  
      long x = 3.0;         // Error: no implicit conversion from double  
long y = (long)3.0;   // OK: explicit conversion  
```  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 <xref:System.Int64?qualifyHint=False>   
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Integral Types Table](../vs140/Integral-Types-Table--C#-Reference-.md)   
 [Built-in Types Table](../Topic/Built-In%20Types%20Table%20\(C%23%20Reference\).md)   
 [Implicit Numeric Conversions Table](../vs140/Implicit-Numeric-Conversions-Table--C#-Reference-.md)   
 [Explicit Numeric Conversions Table](../Topic/Explicit%20Numeric%20Conversions%20Table%20\(C%23%20Reference\).md)