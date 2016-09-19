---
title: "Unsafe Code and Pointers (C# Programming Guide)"
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
ms.assetid: b0fcca10-a92d-4f2a-835b-b0ccae6739ee
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Unsafe Code and Pointers (C# Programming Guide)
To maintain type safety and security, C# does not support pointer arithmetic, by default. However, by using the [unsafe](../vs140/unsafe--C#-Reference-.md) keyword, you can define an unsafe context in which pointers can be used. For more information about pointers, see the topic [Pointer types](../vs140/Pointer-types--C#-Programming-Guide-.md).  
  
> [!NOTE]
>  In the common language runtime (CLR), unsafe code is referred to as unverifiable code. Unsafe code in C# is not necessarily dangerous; it is just code whose safety cannot be verified by the CLR. The CLR will therefore only execute unsafe code if it is in a fully trusted assembly. If you use unsafe code, it is your responsibility to ensure that your code does not introduce security risks or pointer errors.  
  
## Unsafe Code Overview  
 Unsafe code has the following properties:  
  
-   Methods, types, and code blocks can be defined as unsafe.  
  
-   In some cases, unsafe code may increase an application's performance by removing array bounds checks.  
  
-   Unsafe code is required when you call native functions that require pointers.  
  
-   Using unsafe code introduces security and stability risks.  
  
-   In order for C# to compile unsafe code, the application must be compiled with [/unsafe](../Topic/-unsafe%20\(C%23%20Compiler%20Options\).md).  
  
## Related Sections  
 For more information, see:  
  
-   [Pointer types](../vs140/Pointer-types--C#-Programming-Guide-.md)  
  
-   [Fixed Size Buffers (C#)](../Topic/Fixed%20Size%20Buffers%20\(C%23%20Programming%20Guide\).md)  
  
-   [How to: Use Pointers to Copy an Array of Bytes (C#)](../vs140/How-to--Use-Pointers-to-Copy-an-Array-of-Bytes---C#-Programming-Guide-.md)  
  
-   [unsafe](../vs140/unsafe--C#-Reference-.md)  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming](../vs140/C#-Programming-Guide.md)