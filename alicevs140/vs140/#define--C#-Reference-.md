---
title: "#define (C# Reference)"
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
ms.assetid: 23638b8f-779c-450e-b600-d55682de7d01
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #define (C# Reference)
You use `#define` to define a symbol. When you use the symbol as the expression that's passed to the [#if](../vs140/#if--C#-Reference-.md) directive, the expression will evaluate to `true`, as the following example shows:  
  
 `#`  `define`   `DEBUG`  
  
## Remarks  
  
> [!NOTE]
>  The `#define` directive cannot be used to declare constant values as is typically done in C and C++. Constants in C# are best defined as static members of a class or struct. If you have several such constants, consider creating a separate "Constants" class to hold them.  
  
 Symbols can be used to specify conditions for compilation. You can test for the symbol with either [#if](../vs140/#if--C#-Reference-.md) or [#elif](../vs140/#elif--C#-Reference-.md). You can also use the `conditional` attribute to perform conditional compilation.  
  
 You can define a symbol, but you cannot assign a value to a symbol. The `#define` directive must appear in the file before you use any instructions that aren't also preprocessor directives.  
  
 You can also define a symbol with the [/define](../Topic/-define%20\(C%23%20Compiler%20Options\).md) compiler option. You can undefine a symbol with [#undef](../vs140/#undef--C#-Reference-.md).  
  
 A symbol that you define with `/define` or with `#define` does not conflict with a variable of the same name. That is, a variable name should not be passed to a preprocessor directive and a symbol can only be evaluated by a preprocessor directive.  
  
 The scope of a symbol that was created by using `#define` is the file in which the symbol was defined.  
  
 As the following example shows, you must put `#define` directives at the top of the file.  
  
```c#  
#define DEBUG  
//#define TRACE  
#undef TRACE  
  
using System;  
  
public class TestDefine  
{  
    static void Main()  
    {  
#if (DEBUG)  
        Console.WriteLine("Debugging is enabled.");  
#endif  
  
#if (TRACE)  
     Console.WriteLine("Tracing is enabled.");  
#endif  
    }  
}  
// Output:  
// Debugging is enabled.  
```  
  
 For an example of how to undefine a symbol, see [#undef (C# Reference)](../vs140/#undef--C#-Reference-.md).  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Preprocessor Directives](../vs140/C#-Preprocessor-Directives.md)   
 [const (C# Reference)](../vs140/const--C#-Reference-.md)   
 [How to: Compile Conditionally with Trace and Debug](assetId:///56d051c3-012c-42c1-9a58-7270edc624aa)   
 [#undef (C# Reference)](../vs140/#undef--C#-Reference-.md)   
 [#if (C# Reference)](../vs140/#if--C#-Reference-.md)