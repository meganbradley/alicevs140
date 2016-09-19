---
title: "unsafe (C# Reference)"
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
ms.assetid: 7e818009-1c6e-4b9e-b769-3728a01586a0
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unsafe (C# Reference)
The `unsafe` keyword denotes an unsafe context, which is required for any operation involving pointers. For more information, see [Unsafe Code and Pointers (C#)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md).  
  
 You can use the `unsafe` modifier in the declaration of a type or a member. The entire textual extent of the type or member is therefore considered an unsafe context. For example, the following is a method declared with the `unsafe` modifier:  
  
```  
  
      unsafe static void FastCopy(byte[] src, byte[] dst, int count)  
{  
    // Unsafe context: can use pointers here.  
}  
```  
  
 The scope of the unsafe context extends from the parameter list to the end of the method, so pointers can also be used in the parameter list:  
  
```  
  
unsafe static void FastCopy ( byte* ps, byte* pd, int count ) {...}  
```  
  
 You can also use an unsafe block to enable the use of an unsafe code inside this block. For example:  
  
```  
  
      unsafe  
{  
    // Unsafe context: can use pointers here.  
}  
```  
  
 To compile unsafe code, you must specify the [/unsafe](../Topic/-unsafe%20\(C%23%20Compiler%20Options\).md) compiler option. Unsafe code is not verifiable by the common language runtime.  
  
## Example  
 [!CODE [csrefKeywordsModifiers#22](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#22)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [fixed Statement](../vs140/fixed-Statement--C#-Reference-.md)   
 [Unsafe Code and Pointers (C#)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md)   
 [Fixed Size Buffers (C#)](../Topic/Fixed%20Size%20Buffers%20\(C%23%20Programming%20Guide\).md)