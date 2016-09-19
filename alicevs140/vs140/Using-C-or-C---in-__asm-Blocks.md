---
title: "Using C or C++ in __asm Blocks"
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
ms.topic: article
ms.assetid: ae8b2b52-6b75-42e3-ac0c-ad02d922ed97
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using C or C++ in __asm Blocks
## Microsoft Specific  
 Because inline assembly instructions can be mixed with C or C++ statements, they can refer to C or C++ variables by name and use many other elements of those languages.  
  
 An `__asm` block can use the following language elements:  
  
-   Symbols, including labels and variable and function names  
  
-   Constants, including symbolic constants and `enum` members  
  
-   Macros and preprocessor directives  
  
-   Comments (both **/\* \*/** and **//** )  
  
-   Type names (wherever a MASM type would be legal)  
  
-   `typedef` names, generally used with operators such as **PTR** and **TYPE** or to specify structure or union members  
  
 Within an `__asm` block, you can specify integer constants with either C notation or assembler radix notation (0x100 and 100h are equivalent, for example). This allows you to define (using `#define`) a constant in C and then use it in both C or C++ and assembly portions of the program. You can also specify constants in octal by preceding them with a 0. For example, 0777 specifies an octal constant.  
  
## What do you want to know more about?  
  
-   [Using Operators in __asm Blocks](../vs140/Using-Operators-in-__asm-Blocks.md)  
  
-   [Using C or C++ Symbols_in __asm Blocks](../vs140/Using-C-or-C---Symbols-in-__asm-Blocks.md)  
  
-   [Accessing C or C++ Data in __asm Blocks](../vs140/Accessing-C-or-C---Data-in-__asm-Blocks.md)  
  
-   [Writing Functions with Inline Assembly](../vs140/Writing-Functions-with-Inline-Assembly.md)  
  
 **END Microsoft Specific**  
  
## See Also  
 [Inline Assembler](../vs140/Inline-Assembler.md)