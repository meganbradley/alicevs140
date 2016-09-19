---
title: "Overview of File Translation"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: 5036c7b7-ccff-4e2c-b052-a9ea6c71af87
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overview of File Translation
C++ programs, like C programs, consist of one or more files. Each of these files is translated in the following conceptual order (the actual order follows the "as if" rule: translation must occur as if these steps had been followed):  
  
1.  Lexical tokenizing. Character mapping and trigraph processing, line splicing, and tokenizing are performed in this translation phase.  
  
2.  Preprocessing. This translation phase brings in ancillary source files referenced by `#include` directives, handles "stringizing" and "charizing" directives, and performs token pasting and macro expansion (see [Preprocessor Directives](../vs140/Preprocessor-Directives.md) in the *Preprocessor Reference* for more information). The result of the preprocessing phase is a sequence of tokens that, taken together, define a "translation unit."  
  
     Preprocessor directives always begin with the number-sign (**#**) character (that is, the first nonwhite-space character on the line must be a number sign). Only one preprocessor directive can appear on a given line. For example:  
  
    ```  
    #include <iostream>  // Include text of iostream in   
                         //  translation unit.  
    #define NDEBUG       // Define NDEBUG (NDEBUG contains empty   
                         //  text string).  
    ```  
  
3.  Code generation. This translation phase uses the tokens generated in the preprocessing phase to generate object code.  
  
     During this phase, syntactic and semantic checking of the source code is performed.  
  
 See [Phases of Translation](../vs140/Phases-of-Translation.md) in the *Preprocessor Reference* for more information.  
  
 The C++ preprocessor is a strict superset of the ANSI C preprocessor, but the C++ preprocessor differs in a few instances. The following list describes several differences between the ANSI C and the C++ preprocessors:  
  
-   Single-line comments are supported. See [Comments](../vs140/Comments--C---.md) for more information.  
  
-   One predefined macro, **__cplusplus**, is defined only for C++. See [Predefined Macros](../vs140/Predefined-Macros.md) in the *Preprocessor Reference* for more information.  
  
-   The C preprocessor does not recognize the C++ operators: **.\***, **–>\***, and `::`. See [Operators](../vs140/C---Built-in-Operators--Precedence-and-Associativity.md) and [Expressions](../vs140/Expressions--C---.md), for more information about operators.  
  
## See Also  
 [Lexical Conventions](../vs140/Lexical-Conventions.md)