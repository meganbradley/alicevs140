---
title: "Macros (C-C++)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: Macros (C/C++)
ms.assetid: a7bfc5d4-2537-4fe0-bef0-70cec0b43388
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Macros (C-C++)
Preprocessing expands macros in all lines that are not preprocessor directives (lines that do not have a **#** as the first non-white-space character) and in parts of some directives that are not skipped as part of a conditional compilation. "Conditional compilation" directives allow you to suppress compilation of parts of a source file by testing a constant expression or identifier to determine which text blocks are passed on to the compiler and which text blocks are removed from the source file during preprocessing.  
  
 The `#define` directive is typically used to associate meaningful identifiers with constants, keywords, and commonly used statements or expressions. Identifiers that represent constants are sometimes called "symbolic constants" or "manifest constants." Identifiers that represent statements or expressions are called "macros." In this preprocessor documentation, only the term "macro" is used.  
  
 When the name of the macro is recognized in the program source text or in the arguments of certain other preprocessor commands, it is treated as a call to that macro. The macro name is replaced by a copy of the macro body. If the macro accepts arguments, the actual arguments following the macro name are substituted for formal parameters in the macro body. The process of replacing a macro call with the processed copy of the body is called "expansion" of the macro call.  
  
 In practical terms, there are two types of macros. "Object-like" macros take no arguments, whereas "function-like" macros can be defined to accept arguments so that they look and act like function calls. Because macros do not generate actual function calls, you can sometimes make programs run faster by replacing function calls with macros. (In C++, inline functions are often a preferred method.) However, macros can create problems if you do not define and use them with care. You may have to use parentheses in macro definitions with arguments to preserve the proper precedence in an expression. Also, macros may not correctly handle expressions with side effects. See the `getrandom` example in [The #define Directive](../vs140/#define-Directive--C-C---.md) for more information.  
  
 Once you have defined a macro, you cannot redefine it to a different value without first removing the original definition. However, you can redefine the macro with exactly the same definition. Thus, the same definition can appear more than once in a program.  
  
 The #**undef** directive removes the definition of a macro. Once you have removed the definition, you can redefine the macro to a different value. [The #define Directive](../vs140/#define-Directive--C-C---.md) and [The #undef Directive](../vs140/#undef-Directive--C-C---.md) discuss the `#define` and `#undef` directives, respectively.  
  
 For more information, see,  
  
-   [Macros and C++](../vs140/Macros-and-C--.md)  
  
-   [Variadic Macros](../vs140/Variadic-Macros.md)  
  
-   [Predefined Macros](../vs140/Predefined-Macros.md)  
  
## See Also  
 [C/C++ Preprocessor Reference](../vs140/C-C---Preprocessor-Reference.md)