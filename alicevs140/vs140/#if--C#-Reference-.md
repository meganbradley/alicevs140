---
title: "#if (C# Reference)"
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
ms.assetid: 48cabbff-ca82-491f-a56a-eeccd528c7c2
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #if (C# Reference)
When the C# compiler encounters an `#if` directive, followed eventually by an [#endif](../vs140/#endif--C#-Reference-.md) directive, it will compile the code between the directives only if the specified symbol is defined.  Unlike C and C++, you cannot assign a numeric value to a symbol; the #if statement in C# is Boolean and only tests whether the symbol has been defined or not. For example,  
  
```  
#define DEBUG  
// ...  
#if DEBUG  
    Console.WriteLine("Debug version");  
#endif  
```  
  
 You can use the operators [==](../Topic/==%20Operator%20\(C%23%20Reference\).md) (equality), [!=](../Topic/!=%20Operator%20\(C%23%20Reference\).md) (inequality) only to test for [true](../vs140/true--C#-Reference-.md) or [false](../vs140/false--C#-Reference-.md) . True means the symbol is defined. The statement `#if DEBUG` has the same meaning as `#if (DEBUG == true)`. You can use the operators [&&](../vs140/---Operator--C#-Reference-.md) (and), [&#124;&#124;](../vs140/---Operator--C#-Reference-.md) (or), and [!](../Topic/!%20Operator%20\(C%23%20Reference\).md) (not) to evaluate whether multiple symbols have been defined. You can also group symbols and operators with parentheses.  
  
## Remarks  
 `#if`, along with the [#else](../vs140/#else--C#-Reference-.md), [#elif](../vs140/#elif--C#-Reference-.md), [#endif](../vs140/#endif--C#-Reference-.md), [#define](../vs140/#define--C#-Reference-.md), and [#undef](../vs140/#undef--C#-Reference-.md) directives, lets you include or exclude code based on the existence of one or more symbols. This can be useful when compiling code for a debug build or when compiling for a specific configuration.  
  
 A conditional directive beginning with a `#if` directive must explicitly be terminated with a `#endif` directive.  
  
 `#define` lets you define a symbol, such that, by using the symbol as the expression passed to the `#if` directive, the expression will evaluate to `true`.  
  
 You can also define a symbol with the [/define](../Topic/-define%20\(C%23%20Compiler%20Options\).md) compiler option. You can undefine a symbol with [#undef](../vs140/#undef--C#-Reference-.md).  
  
 A symbol that you define with `/define` or with `#define` does not conflict with a variable of the same name. That is, a variable name should not be passed to a preprocessor directive and a symbol can only be evaluated by a preprocessor directive.  
  
 The scope of a symbol created with `#define` is the file in which it was defined.  
  
## Example  
  
```  
// preprocessor_if.cs  
#define DEBUG#define MYTEST  
using System;  
public class MyClass   
{  
    static void Main()   
    {  
#if (DEBUG && !MYTEST)  
        Console.WriteLine("DEBUG is defined");  
#elif (!DEBUG && MYTEST)  
        Console.WriteLine("MYTEST is defined");  
#elif (DEBUG && MYTEST)  
        Console.WriteLine("DEBUG and MYTEST are defined");  
#else  
        Console.WriteLine("DEBUG and MYTEST are not defined");  
#endif  
    }  
}  
```  
  
 **DEBUG and MYTEST are defined**   
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Preprocessor Directives](../vs140/C#-Preprocessor-Directives.md)